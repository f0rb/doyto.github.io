# 中间表操作

### 表结构

```sql
create table t_user_and_role (user_id bigint, role_id int);
```

### 定义

```java
@Bean
public AssociativeService<Long, Integer> userAndRoleAssociativeService() {
    return new TemplateAssociativeService<>("t_user_and_role", "userId", "roleId");
}
```

### 使用

```java
@RestController
class AuthController {
    @Resource
    AssociativeService<Long, Integer> userAndRoleAssociativeService;

    @GetPostMapping("reallocateRolesForUser")
    public void reallocateRoles(Long userId, @RequestParam List<Integer> roleIds) {
        userAndRoleAssociativeService.reallocateForLeft(userId, roleIds);
    }
}

```

### 访问

访问该接口将执行以下 SQL语句

```sql
DELETE FROM t_user_and_role WHERE userId = ?
INSERT INTO t_user_and_role (userId, roleId) values (?, ?)[, (?, ?)]
```

