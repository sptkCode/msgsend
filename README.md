# ronglianyun
golang 容联云sdk, 使用的是短信模板1---您的验证码是123456, 请于5分钟内正确输入

# usage:
   git clone 到 自己的gopath的src目录
   
# example
   import "sendmsm"  
   //accountSid 容联云账户id  
   //authorToken 容联云用户验证令牌  
   // appId 容联云商配置的应用id  

   // 使用NewRLYSMS创建发送短信消息的对象  
   sms:=NewRLYSMS(accountSid,authorToken,appId)  

   // 发送消息demo  
   // 参数一 要发送的消息  
   // 参数二 模板1需要的 请于{int}分钟内正确输入  
   // 参数三可变参数 批量发送消息，可以添加多个手机号码  
   sms.SendMsMs("253536",2,"158xxxxxx")   
