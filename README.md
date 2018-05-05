# 微信支付demo(spring mvc)

原文参考链接： [https://blog.csdn.net/zhourenfei17/article/details/77765585](https://blog.csdn.net/zhourenfei17/article/details/77765585)

支付流程步骤：

1）首先调用wx.login方法获取code，通过code获取openid；

2）java后台调用统一下单支付接口（这里会进行第一次签名），用来获取prepay_id；

3）java后台再次调用签名（这里会进行第二次签名），并返回支付需要用使用的参数；

4）小程序前端wx.requestPayment方法发起微信支付；

5）java后台接收来自微信服务器的通知并处理结果。

详细步骤可参考：[https://pay.weixin.qq.com/wiki/doc/api/wxa/wxa_api.php?chapter=7_4&index=3](https://pay.weixin.qq.com/wiki/doc/api/wxa/wxa_api.php?chapter=7_4&index=3)

Spring Boot版本仓库：[https://github.com/Gitsifu/we-pay-sb](https://github.com/Gitsifu/we-pay-sb)
