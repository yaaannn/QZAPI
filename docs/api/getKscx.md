#考试信息
获取考试信息
注意：条件所限制，暂未明晰

##请求
``` url
GET http://教务系统URL/app.do?
```
##请求参数
```js
request.header{token:'运行身份验证authUser时获取到的token，有过期机制'},
request.data{
			'method':'getKscx',  //必填
			'xh':'2017168xxxxx',  //条件所限制，暂未明晰
			}
```

##返回
``` json
条件所限制，暂未明晰
```

##例程
``` url
GET http://教务系统URL/app.do?method=getKscx&xh=201716xxxxx
```