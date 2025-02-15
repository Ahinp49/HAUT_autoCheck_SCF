## HAUT_autoCheck

**河南工业大学完美校园健康打卡 腾讯云函数版**
本项目基于原[YooKing的HAUT_autoCheck](https://github.com/YooKing/HAUT_autoCheck/)项目开发

- 随机温度(36.2℃-36.8℃)🌡，随机经纬度🌍
- 多人打卡👨‍👩‍👧‍👧，一人微信通知全部打卡结果💬
- 校内外打卡:11:00-15:00🕑
- 基于腾讯云函数，完全解放你的设备和服务器✔
- 有任何问题可以提交[issues](https://github.com/Revincx/HAUT_autoCheck/issues/new)

## 使用方法 

1. 使用git克隆仓库代码到本地，去[腾讯云控制台](https://console.cloud.tencent.com/scf/)新建一个函数

2. 创建方式选择自定义创建，运行环境选择Python 3.6,选择本地上传zip包,然后把刚才的代码打包上传上去(注意代码直接放在根目录),地域选国内的基本都行，执行超时时间尽量改成10秒到20秒左右，否则有概率会超时，其他的不要改

3. 展开高级配置选项卡，在环境变量里添加以下变量：

|key|value|
|---|---|
|sckey|Sever酱推送服务的SCKEY|
|user1|用户1的手机号+英文逗号+密码|
|user2|用户2的手机号+英文逗号+密码|
| ... | ... |

多个用户以此类推

4. 展开触发器配置选项卡，选择自定义创建，触发方式选择定时触发，触发周期选择自定义触发周期，Cron表达式填写`0 0 9 * * * *`（腾讯云函数基于北京时间，此处即指北京时间每天上午9点）

5. 点击完成并部署即可

本项目目前仍在测试，有bug欢迎大家提出并讨论。

## 许可
本项目以 MIT 协议开源，详情请见 [LICENSE](LICENSE) 文件。
