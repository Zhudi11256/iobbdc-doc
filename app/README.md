# APP接口文档

## 鉴权机制
### 通过 header 提交Token
```
X-AUTH-TOKEN
```

## APP广告位和编码

| 位置 | code | 广告类型 |说明|
| :-----| :---- | :---- | :---- |
| 启动广告 | start_page | 图片 | |
| 首页banner滚动广告 | index_banner | 图片 | 首页以及首页视频列表顶部的滚动广告|
| 首页feed流广告 | index_feed | 图片 |每隔一个主题，展示一个广告|
| 播放页banner广告 | play_banner | 图片 | |
| 播放暂停广告 | play_pause | 图片 | |
| 个人主页banner广告 | user_pofile_banner | 图片 | |
| 福利广告|welfare|图片||
| 视频播放定时广告|play_timing|图片||
| 直播平台广告|live_plat|图片||
| 直播房间广告|live_room|图片||

## 数据校验规则

| 数据 | 正则 | 说明|
| :-----| :---- | :---- |
| 手机号码 | `^1[3-9]\\d{9}$` | 只能是大陆手机号码 |
| 用户密码 | `^.{6,32}$` | 6 - 32位长度，不能包含换行符 |

