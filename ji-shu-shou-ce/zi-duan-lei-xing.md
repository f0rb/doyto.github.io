# 数据库方言

## Getting Super Powers

{% code title="win.doyto.query.core.Dialect.java" %}
```java
public interface Dialect {
    String buildPageSql(String sql, int limit, long offset);

    default String wrapLabel(String fieldName) {
        return fieldName;
    }
}
```
{% endcode %}

Becoming a super hero is a fairly straight forward process:

```
$ give me super-powers
```

{% hint style="info" %}
 Super-powers are granted randomly so please submit an issue if you're not happy with yours.
{% endhint %}

Once you're strong enough, save the world:



