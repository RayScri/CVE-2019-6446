## CVE-2019-6446 Numpy反序列化命令执行
NumPy是一个功能强大的Python库，主要用于对多维数组执行计算。大佬们分析称其版本小于等于1.16.0存在该漏洞，修复建议是删除lib/npyio.py中load函数的参数allow_pickle或将其值改为False就可以避免反序列化问题；在测试1.16.3（Mac/Windows）版本该load函数移除了allow_pickle参数。但依旧存在命令执行。
测试时最新版本为1.16.3

![如图](https://github.com/RayScri/CVE-2019-6446/blob/master/WechatIMG194.png)


Reference:https://mp.weixin.qq.com/s/9qwTTtQdpIjH8f0CcDYs6g
