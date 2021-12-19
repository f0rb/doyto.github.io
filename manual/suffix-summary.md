# 查询对象字段后缀汇总

| 后缀名称    | 操作符         | 占位符                                    | 类型限制       | 值处理     |
| ------- | ----------- | -------------------------------------- | ---------- | ------- |
| -       | =           | ？                                      |            |         |
| Not     | !=          | ?                                      |            |         |
| NotLike | NOT LIKE    | ?                                      | String     | %value% |
| Like    | LIKE        | ?                                      | String     | %value% |
| Start   | LIKE        | ?                                      | String     | %value  |
| End     | LIKE        | ?                                      | String     | value%  |
| NotIn   | NOT IN      | <p>集合非空时：(?[, ?]) <br>集合为空时：忽略</p>     | Collection |         |
| In      | IN          | <p>集合非空时：(?[, ?]) <br>集合为空时：(null)</p> | Collection |         |
| NotNull | IS NOT NULL | -                                      | boolean    |         |
| Null    | IS NULL     | -                                      | boolean    |         |
| Gt      | >           | ?                                      |            |         |
| Ge      | >=          | ?                                      |            |         |
| Lt      | <           | ?                                      |            |         |
| Le      | <=          | ?                                      |            |         |
| Eq      | =           | ?                                      |            |         |

