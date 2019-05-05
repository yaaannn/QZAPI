#用户信息
获取当前token的用户信息
注意：此API测试与参考文档不同，待修改/补充

##请求
``` url
GET http://jwxt.xxxx.edu.cn/app.do?method=getStudentIdInfo&xh={$学号}
```

##参数
```js
request.header{token:'运行身份验证authUser时获取到的token，有过期机制'},
request.data{
	'method':'getStudentIdInfo',  //必填
	'xh':'2017168xxxxx'  //疑似非必填，添加或不添加本参数返回相同值
}
```

##返回
``` json
{
	'flag':"0"
}
```

##例程
``` url
GET http://jwxt.xxxx.edu.cn/app.do?method=getStudentIdInfo&xh=101010000
```