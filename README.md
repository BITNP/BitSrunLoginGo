# BitSrunLoginGo

深澜校园网登录脚本Go语言版。GO语言可以直接交叉编译出mips架构可执行程序（路由器）（主流平台更不用说了），从而免除安装环境。

代码逻辑来自 https://github.com/coffeehat/BIT-srun-login-script

首次运行将生成Config.json文件

Config.json说明：

```json5
{
 "from": {
  "domain": "www.msftconnecttest.com", //登录地址ip或域名
  "username": "", //账号
  "user_type": "", //运营商类型，详情看下方
  "password": "" //密码
 },
 "meta": { //登录参数
  "n": "200",
  "type": "1",
  "acid": "5",
  "enc": "srun_bx1"
 },
 "settings": {
  "quit_if_net_ok": false, //登陆前是否检查网络
  "demo_mode": false, //测试模式，报错更详细，且生成运行日志与错误日志
  "dns": "1.2.4.8" //检查网络用的DNS地址，建议设为网关分发的内网DNS地址
 }
}
```

登录参数从原网页登陆时对`/srun_portal`的请求抓取

运营商类型在原网页会被自动附加在账号后，请把`@`后面的部分填入`user_type`