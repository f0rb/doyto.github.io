# Query

在Query对象中可以通过添加不同后缀的字段并赋值，从而在执行过程中生成不同的SQL查询语句。

先看一个例子

```java
@SuperBuilder
@NoArgsConstructor
public class TestQuery extends PageQuery {
    private Integer id;
    private Integer idLt;
    private Integer idLe;
    private List<Integer> idIn;
    private List<Integer> idNotIn;
    private String usernameLike;
}
```

我们通过一个单元测试用例来看一下将TestQuery的字段都赋值后对应生成的SQL语句：

