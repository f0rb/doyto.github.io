# Query对象字段映射

## 后缀使用

在Query对象中可以通过添加不同后缀的字段并赋值，从而在执行过程中生成不同的SQL查询语句。

* Not\("!="\)
* NotLike\("NOT LIKE"\)
* Start\("LIKE"\)
* Like\("LIKE"\)
* NotIn\("NOT IN"\)
* In\("IN"\)
* NotNull\("IS NOT NULL"\)
* Null\("IS NULL"\)
* Gt\("&gt;"\)
* Ge\("&gt;="\)
* Lt\("&lt;"\)
* Le\("&lt;="\)
* NONE\("="\)

## 注解使用

* @QueryTableAlias
* @NestedQueries
* @QueryField

