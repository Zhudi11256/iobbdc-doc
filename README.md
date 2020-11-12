# 流光视频文档接口

## 通用的JSON通信格式
```json
{
    "message": "ok",    // 消息提示
    "success": true,    // 业务是否执行成功
    "code": 0,      // 状态码
    "data": {}  // 数据检索接口，返回检索的数据，json对象或者数组
}
```
### 状态码详情
```java
OK(0, "ok"),
NOT_FOUND(1, "资源不存在"),
UNAUTHORIZED(2, "未登录"),
FORBIDDEN(3, "无权操作"),
BAD_REQUEST(4, "非法请求"),
REQUIRED_VERIFY_CODE(5, "需要验证码"),
VERIFY_CODE_FAIL(6, "验证码错误"),
PHONE_CAPTCHA_FAIL(7, "短信验证码错误"),
ALREADY_REGISTERED(8, "手机号码已经注册"),
GAME_PARAME_ERROR(9,"游戏参数错误"),
INSUFFICIENT_BALANCE(10, "余额不足"),
REQUEST_LIMIT(11, "请求被限制"),
PHONE_NOT_REGISTER(12, "手机号码未注册"),
PHONE_ALREADY_BOUND(13, "手机号码已经绑定"),
INTERNAL_SERVER_ERROR(999, "服务器异常");
```

