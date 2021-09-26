# 数据库方言

## 涉及组件

{% code title="Dialect.java" %}
```java
package win.doyto.query.core;

public interface Dialect {
    String buildPageSql(String sql, int limit, long offset);
    default String wrapLabel(String fieldName) {
        return fieldName;
    }
}
```
{% endcode %}

## 使用说明

Dialect接口为针对不同的数据库，提供了一个扩展接口Dialect，通过实现该接口对原始sql语句添加分页语法

## 参考实现

```java
public class HSQLDBDialect implements Dialect {
    @Override
    public String buildPageSql(String sql, int limit, long offset) {
        return sql + " LIMIT " + limit + (sql.startsWith("SELECT") ? " OFFSET " + offset : "");
    }
}
```

## 配置实现

### 方式一：yml文件

{% code title="application.yml" %}
```yaml
doyto:
  query:
    config:
      dialect: win.doyto.query.demo.common.HsqldbDialect
```
{% endcode %}

### 方式二：静态方法

```java
GlobalConfiguration.instance().setDialect(new HSQLDBDialect())
```

