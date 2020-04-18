#考试信息
获取考试信息

##请求
``` url
GET http://jwxt.xxxx.edu.cn/app.do?method=getKscx&xh={$学号}
```

##参数
```js
request.header{token:'运行身份验证authUser时获取到的token，有过期机制'},
request.data{
	'method':'getKscx',  //必填
	'xh':'2017168xxxxx',  //学号
}
```

##返回
>数据格式来源强智2017版教务系统
``` json
[
  {
    "ksqssj": "2019-12-31 14:00~15:40",  //考试起始结束时间
    "ksjc": "第17周星期一第五六节",  //考试节次
    "xm": "",  //姓名
    "bj": "",  //班级
    "bz": null,  //备注
    "ksmc": "",  //考试名称，例如："电气学院2019-2020-1期末考试"
    "kcmc": "",  //课程名称(即考试科目名称)，例如，"高等数学1"
    "jsmc": ""  //教室名称(即考试地点)，例如，"电气楼101"
   },
  {
    "ksqssj": ,
    "ksjc": ,
    "xm": ,
    "bj": ,
    "bz": ,
    "ksmc": ,
    "kcmc":,
    "jsmc": 
  }
]
```

##例程
``` url
GET http://jwxt.xxxx.edu.cn/app.do?method=getKscx&xh=201716xxxxx
```
