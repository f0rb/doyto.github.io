# 嵌套查询

DoytoQuery通过解析字段上配置的@NestedQueries和@NestedQuery注解来为字段生成嵌套查询语句。

注解定义如下：

{% code title="NestedQueries.java" %}
```java
@Target(FIELD)
@Retention(RUNTIME)
public @interface NestedQueries {

    String column() default "id";

    String op() default "IN";

    boolean appendWhere() default true;

    NestedQuery[] value();

}
```
{% endcode %}

{% code title="NestedQuery.java" %}
```java
public @interface NestedQuery {

    String select();

    String from();

    String extra() default "";

    String op() default "IN";

}
```
{% endcode %}

## 代码示例

### 简单嵌套查询

假设一个具有层级关系的菜单表，子菜单的parent\_id指向父菜单的id，这样可以通过如下语句查询出所有的父菜单：

```sql
SELECT * FROM menu WHERE id IN (SELECT parent_id FROM menu)
```

通过DoytoQuery执行该查询，需要创建对应的MenuQuery类，并添加一个用于查询的字段，配置@NestedQueries注解：

```java
public class MenuQuery extends PageQuery {
    @NestedQueries({
            @NestedQuery(select = "parent_id", from = "menu")
    })
    private boolean onlyParent;
}
```

编写一个单元测试看下效果：

```java
@Test
public void testNestedQuery() {
    MenuQuery menuQuery = MenuQuery.builder().onlyParent(true).build();

    ArrayList<Object> argList = new ArrayList<>();
    String sql = BuildHelper.buildWhere(menuQuery, argList);

    String expected = " WHERE id IN (SELECT parent_id FROM menu)";
    assertEquals(expected, sql);
    assertTrue(argList.isEmpty());
}
```

 测试通过。

在MenuQuery中，@NestedQueries注解中的column和op字段的默认值合起来为"id IN"，@NestedQuery\(select = "parent\_id", from = "menu"\)括号内的内容去掉符号后就是：\(select parent\_id from menu\)，两条语句合起来再将关键字修改为大写，即为：id IN \(SELECT parent\_id FROM menu\)。









 

