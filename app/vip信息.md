# VIP
## vip列表
- `/api/vip`
- `GET`
- `request`

| 参数名称 | 数据类型 | 是否必须 |参数说明|默认值|参数示例|
| :-----| :---- | :---- | :---- | :---- | :---- |

- `resonse`
```json
{
    "message": "ok",
    "success": true,
    "code": 0,
    "data": [{
        "id": 1,
        "title": "一个月vip",
        "vipTime": 2,
        "vipTimeUnit": "MINUTES",// vip时间单位
        "price": "28"
    }]
}
```
- vip时间单位枚举
```
MINUTES     分钟
HOURS       小时
DAYS        天
WEEKS       周
MONTHS      月
YEARS       年
FOREVER     永久
```

## vip购买
- `/api/vip/order`
- `GET`
- `request`

| 参数名称 | 数据类型 | 是否必须 |参数说明|默认值|参数示例|
| :-----| :---- | :---- | :---- | :---- | :---- |
| id | int | 是 | 商品id|||
| vipTime | int | 是 | vip时间|||
| vipTimeUnit | 是|string | vip时间单位，枚举|||
| price | string | 是 | 价格|||

- `resonse`
```json
{
    "message": "ok",
    "success": true,
    "code": 0
}
```

## vip购买记录
- `/api/vip/history`
- `GET`
- `request`

| 参数名称 | 数据类型 | 是否必须 |参数说明|默认值|参数示例|
| :-----| :---- | :---- | :---- | :---- | :---- |
| page | int | 是 | 页码|||
| rows | int | 是 | 每页显示数量|||
| startDate | string | 否 |过滤参数，开始日期||2019-05-03|
| endDate | string | 否 |过滤参数，结束日期||2019-05-08|
- `resonse`
```json
{
    "message": "ok",
    "success": true,
    "code": 0,
    "data": {
        "total": 100,
        "rows": [{
            "id": 1,            // 记录id
            "orderNumber": "XX5555",    // 订单号
            "amount": "25.8",  // 金额  
            "createdDate": "2020-08-01 16:50:14",       // 创建日期
            "snapshot": "{\"title\"： \"一个月vip\"}"       // 商品信息
        }]
    }
}
```