# 大麦辅助 - 抢票脚本

> 2023.05.05 修改使抢票脚本对部分演唱会有效
> 
> 2023.05.09 对应页面更新了class_name, 但是出现新机制触发机器验证无法完成下单
>
> 2023.05.12 增加日期选择
>
> 2023.05.13 补充说明
> # 这就是一个傻逼脚本 请勿使用 不如手工抢票
> # 本来想抢五月天深圳演唱会门票 结果在最后一部卡住了
> # 并且无法手动点击提交 非常傻逼 
> # 技术不够 想删库了

## 依赖
- selenium
>pip install selenium 

## 配置文件

```json
{
    "date": [
        14
    ],
    "sess": [
        1,
        2
    ],
    "price": [
        1,
        2,
        3,
        4,
        5,
        6
    ],
    "real_name": [
        1
    ],
    "nick_name": "",
    "ticket_num": 1,
    "viewer_person": [
        2
    ],
    "driver_path": "C:\\Program Files\\Google\\Chrome\\Application\\chromedriver.exe",
    "damai_url": "https://www.damai.cn/",
    "target_url": "https://m.damai.cn/damai/detail/item.html?itemId=708250808776&spm=a2o71.home.snatch_ticket.item&from=appshare&sqm=dianying.h5.unknown.value.hlw_a2o71_28004194",
    "comment": {
        "title": "comment 下的所有内容为自定义注释,无实际含义",
        "date": "日期序号,仅支持一个日期选择",
        "sess": "场次序号,优先选中的场次序号放在前,填写的场次序号若大于实际场次序号,则会选中实际场次序号最大的",
        "price": "票档序号,优先选中的票档序号放在前,填写的票档序号若大于实际票档序号,则会选中实际票档序号最大的",
        "real_name": "实名者序号,已经弃用",
        "nick_name": "用户昵称,已经弃用",
        "ticket_num": "购买票数,购买票数与观影人序号的数量务必一致",
        "viewer_person": "观影人序号(预先添加实名观影人),优先选中的序号放在前,填写的序号若大于实际序号,则会放弃选中",
        "driver_path": "驱动地址",
        "damai_url": "大麦首页地址,用于登录",
        "target_url": "购票的实际地址,需要使用手机端的地址,域名: https://m.damai.cn/ 开头",
        "queue": {
            "title": "列入待抢的链接地址",
            "zhoujielun_0403": "https://m.damai.cn/damai/detail/item.html?itemId=607865020360&from=appshare&sqm=dianying.h5.unknown.value.hlw_a2o71_28004194&prev_page=8hu5vjnq54&spm=a2o71.28004194.785344.item_horizontal_3"
        }
    }
}

```

## 注意事项

1. 账号必须先做好实名制认证，并添加至少一个实名制的人的信息
2. 第一次打开后会进入登录页面，需要手动选择扫码登陆
3. 如果太久没用，需要先清空目录下的 cookie 文件，然后在重新登录
