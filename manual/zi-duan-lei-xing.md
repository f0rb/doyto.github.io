# 数据库方言

## win.doyto.query.core.Dialect

Dialect接口为针对不对的数据库，提供了一个扩展

```java
public interface Dialect {
    String buildPageSql(String sql, int limit, long offset);

    default String wrapLabel(String fieldName) {
        return fieldName;
    }
}
```





