#学年学期信息
获取学年学期信息

##请求
``` url
GET http://jwxt.xxxx.edu.cn/app.do?method=getXnxq
```

##参数
```js
request.header{token:'运行身份验证authUser时获取到的token，有过期机制'},
request.data{
	'method':'getXnxq' , //必填
	'xh':'2017xxxxxx'  //非必填
}
```

##返回
``` json
[
    {
        "isdqxq": "0",  //是否是当前学期
        "xqmc": "2021-2022-2",  //学期名称
        "xnxq01id": "2021-2022-2"  //学期ID
    },
    {
        "isdqxq": "1",
        "xqmc": "2021-2022-1",
        "xnxq01id": "2021-2022-1"
    }
]
```

##例程
``` url
GET http://jwxt.xxxx.edu.cn/app.do?method=getXnxq
```