#账号信息
获取账号信息

##请求
``` url
GET http://jwxt.xxxx.edu.cn/app.do?method=getUserInfo&xh={$学号}
```

##参数
```js
request.header{token:'运行身份验证authUser时获取到的token，有过期机制'},
request.data{
	'method':'getUserInfo',  //必填
	'xh':'201713984' //学号，必填，可以填写非本token学号获取其他人信息
}
```

##返回
``` json
{
    "fxzy": "无",  //辅修专业
    "xh": "201716xxxx",  //学号
    "xm": "某某某",  //姓名
    "dqszj": "2017",  //未知
    "usertype": "2",  //用户类型
    "yxmc": "信息科学技术学院",  //院系名称
    "xz": 4,  //学制
    "bj": "计算机类2017-10",  //班级
    "dh": "13600000000",  //电话
    "email": "1540000000@qq.com",  //电子邮箱
    "rxnf": "2017",  //入学年份
    "xb": "男",   //性别
    "ksh": "00000000000",  //高考考号
    "nj": "2017",  //年级
    "qq": null,  //QQ号码
    "zymc": "计算机类(计算机科学与技术、网络工程、信息安全)"  //专业名称
}
```

##例程
``` url
GET http://jwxt.xxxx.edu.cn/app.do?method=getUserInfo&xh=201713984
```