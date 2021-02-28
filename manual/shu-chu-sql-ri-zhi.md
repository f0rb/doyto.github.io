# 输出SQL日志



如果需要查看生成的SQL语句，只需要将win.doyto.query.core.SqlAndArgs的日志等级配置为debug即可。

在spring的yaml文件里配置如下：

{% code title="application.yml" %}
```yaml
logging:
  level:
    win.doyto.query.core.SqlAndArgs: debug
```
{% endcode %}

日志打印如下：

```text
...
2021-02-25 22:17:18.442 DEBUG 80237 --- [           main] win.doyto.query.core.SqlAndArgs          : SQL  : SELECT platform, parentId, menuName, memo, valid, id, createUserId, createTime, updateUserId, updateTime FROM menu_01 WHERE id = ?
2021-02-25 22:17:18.442 DEBUG 80237 --- [           main] win.doyto.query.core.SqlAndArgs          : Param: 3(java.lang.Integer)
2021-02-25 22:17:18.447 DEBUG 80237 --- [           main] win.doyto.query.core.SqlAndArgs          : SQL  : DELETE FROM menu_01 WHERE id = ?
2021-02-25 22:17:18.447 DEBUG 80237 --- [           main] win.doyto.query.core.SqlAndArgs          : Param: 3(java.lang.Integer)
...
```



