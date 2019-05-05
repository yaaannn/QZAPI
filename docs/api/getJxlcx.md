#校区教学楼信息
获取校区教学楼信息

##请求
``` url
GET http://教务系统URL/app.do?
```
##请求参数
```js
request.header{token:'运行身份验证authUser时获取到的token，有过期机制'},
request.data{
			'method':'getJxlcx',  //必填
            'xqid':'1'  //非必填，默认值未知
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
GET http://教务系统URL/app.do?method=getJxlcx&xqid=1
```