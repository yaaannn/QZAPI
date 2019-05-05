#教学楼信息
获取某个校区教学楼信息

##请求
``` url
GET http://jwxt.xxxx.edu.cn/app.do?method=getJxlcx&xqid={$校区ID}
```

##参数
```js
request.header{token:'运行身份验证authUser时获取到的token，有过期机制'},
request.data{
	'method':'getJxlcx',  //必填
	'xqid':'1'  //校区ID
}
```

##返回
``` json
[
    {
        "jzwid": "51",  //教学楼ID
        "jzwmc": "画室楼(临时)"  //教学楼名称
    },
    {
        "jzwid": "52",
        "jzwmc": "室外楼(临时)"
    }
]
```

##例程
``` url
GET http://jwxt.xxxx.edu.cn/app.do?method=getJxlcx&xqid=1
```