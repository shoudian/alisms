
# 阿里大于的短信扩展


## 描述

阿里大于的短信扩展

附上:

项目GitHub地址:[https://github.com/shoudian/alisms.git](https://github.com/shoudian/alisms.git "项目Git地址")


## 安装PhalApi2-JWT

在项目的composer.json文件中，添加：

```
{
    "require": {
        "shoudian/alisms": "dev-master"
    }
}
```

配置好后，执行composer update更新操作即可。

## 配置文件
我们需要在 **./config/app.php** 配置文件中追加以下配置：

```
    /**
     * 扩展类库 - 阿里云短信接口配置参数
     */
	'alisms'=>array(
		'accessKeyId'=>'LTAI29s44dxfqxYY',
		'accessKeySecret'=>'ZW6cPTXGZp4ATVaC5WaWL7GCTip8FK',
		'SignName'=>'商呼',
		'charset'=>'UTF-8',
    ),

```

## 入门使用

初始化PhalApi2-JWT,在config/di.php中加入如下代码

```

//阿里云短信扩展
$di->alisms = new \Shoudian\AliSms\Lite();

```

常用基础操作(具体API可以查阅代码中src/Lite.php)

```
// 发送短信
\PhalApi\DI()->alisms->sendSms($config,$mobile,$tplId,$tplParam);
    
```


**如果大家有更好的建议可以私聊或加入到PhalApi大家庭中前来一同维护PhalApi**
**注:笔者能力有限有说的不对的地方希望大家能够指出,也希望多多交流!**
