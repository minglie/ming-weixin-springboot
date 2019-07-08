当普通微信用户向公众账号发消息时，微信服务器将POST消息的XML数据包到开发者填写的URL上。

接收文本消息 
例如用户给公众号发送消息“欢迎开启公众号开发者模式”，在开发者后台收到的公众平台发送的消息xml如下

<xml>
<ToUserName><![CDATA[公众号]]></ToUserName>
 <FromUserName><![CDATA[粉丝号]]></FromUserName>
 <CreateTime>1460537339</CreateTime>
 <MsgType><![CDATA[text]]></MsgType>
 <Content><![CDATA[欢迎开启公众号开发者模式]]></Content>
 <MsgId>6272960105994287618</MsgId>
 </xml>

被动回复文本消息 
即公众号回复用户的文本消息 
1） 被动回复消息，即发送被动响应消息，不同于客服消息接口 
2） 它其实并不是一种接口，而是对微信服务器发过来消息的一次回复 
3） 收到粉丝消息后不想或者不能5秒内回复时，需回复“success”字符串（下文详细介绍） 
4） 客服接口在满足一定条件下随时调用

回复的消息

<xml>
 <ToUserName><![CDATA[粉丝号]]></ToUserName>
 <FromUserName><![CDATA[公众号]]></FromUserName>
 <CreateTime>1460541339</CreateTime>
 <MsgType><![CDATA[text]]></MsgType>
 <Content><![CDATA[test]]></Content>
 </xml>