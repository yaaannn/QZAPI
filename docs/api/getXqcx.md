#校区信息
获取校区信息

##请求
``` url
GET http://教务系统URL/app.do?
```
##请求参数
```js
request.header{token:'运行身份验证authUser时获取到的token，有过期机制'},
request.data{
			'method':'getXqcx'  //必填
			}
```

##返回
``` json
[
    {
        "xqid": "1",  //校区ID
        "xqmc": "儋州校区"  //校区名称
    },
    {
        "xqid": "2",
        "xqmc": "城西校区"
    },
    {
        "xqid": "3",
        "xqmc": "海甸校区"
    }
]
```

##例程
``` url
GET http://教务系统URL/app.do?method=getXqcx
```