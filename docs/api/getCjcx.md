#成绩信息
获取成绩信息

##请求
``` url
GET http://教务系统URL/app.do?
```
##请求参数
```js
request.header{token:'运行身份验证authUser时获取到的token，有过期机制'},
request.data{
			'method':'getCjcx',  //必填
			'xh':'2017168xxxxx',  //必填，可以添加非本token学号查询他人成绩
            'xqxnid':'2017-2018-2' //非必填，不填输出全部成绩
			}
```

##返回
``` json
[
    {
        "bz": null,  //未知
        "cjbsmc": null,  //未知
        "kclbmc": "必修", //课程类别名称
        "zcj": "88",  //总成绩
        "xm": "某某某",  //学生姓名
        "xqmc": "2017-2018-2",  //学期名称
        "kcxzmc": "公共基础课",  //课程性质名称，根据此项不同值可判断该科成绩是否计入GPA
        "kcywmc": "College students career development and guidance",  //课程英文名称
        "ksxzmc": "正常考试",  //考试性质名称,目前遇见的情况有正常考试，补考（x），重修（x），分别意为补考第x次和重修第x次，若补考未通过，正常考试条目和补考条目将同时存在，若补考通过，则只存在补考条目
        "kcmc": "大学生职业发展与就业指导",  //课程名称
        "xf": 1  //学分
    }
]
```

##例程
``` url
GET http://教务系统URL/app.do?method=getCjcx&xh=201716xxxxx&xnxqid=2017-2018-2
```