# @JsonBody

## 注解使用

注解在Controller的类上，所有mapping方法的返回值都会被包装在`JsonResponse`的`data`字段 。

注解在Controller的mapping方法上，仅该方法的返回值会被包装。

### 示例

* 使用

```java
@RestController
@RequestMapping("user")
@JsonBody
public class UserController extends AbstractRestController<UserEntity, Long, UserQuery, UserRequest, UserResponse> {
    ...
}
```

* 返回值

```javascript
{
  "code": "0",
  "message": "ok"
  "data": {}
}
```

 

 



