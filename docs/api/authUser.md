#登录
登录帐号

##请求
``` url
GET http://jwxt.xxxx.edu.cn/app.do?method=authUser&xh={$学号}&pwd={$密码}
```

##参数
```js
request.data{
	"method":'authUser',  //必填
	"xh":'登陆教务系统使用的学号',  //必填
	"pwd":'登陆教务系统需要的密码'  //必填
}
```

##返回
``` json
{
	"flag":"1", //是否成功 #成功1 失败0
	"userrealname":"张三", //用户真实姓名 #失败 null
	"token":"", //令牌，调用其它API时需要附带到HTTP请求header中的token参数中 #失败 -1
	"userdwmc":"XXXX学院", //用户所在学院名称 #失败 null
	"usertype":"2", //用户类别 #已知学生身份为2 失败 null
	"msg":"登录成功" //返回消息
}
```

##例程
``` url
GET http://jwxt.xxxx.edu.cn/app.do?method=authUser&xh=17111111&pwd=1234578

```