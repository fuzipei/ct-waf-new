# 长亭雷池WAF防火墙——动态防护体验

最近雷池更新，发现更新了一个动态防护，于是也给我们的雷池也更新了功能

# 先给大家介绍一下什么是雷池的动态防护
雷池WAF的动态防护功能主要通过将网站中的HTML、JS等内容加密为不同的形式，以此来阻止爬虫和攻击自动化程序的分析。此外，雷池还采用了智能语义分析算法，这种算法能够精准检测攻击行为，具有低误报和难以绕过的特点。
![title](src\background.jpg)

# 安装以及配置流程


访问雷池官网[点击访问雷池官网文档](https://docs.waf-ce.chaitin.cn/zh/%E4%B8%8A%E6%89%8B%E6%8C%87%E5%8D%97/%E5%AE%89%E8%A3%85%E9%9B%B7%E6%B1%A0 "安装文档")。
官网提供了很多种安装方法
或者输入一键安装命令
```
bash -c "$(curl -fsSLk https://waf-ce.chaitin.cn/release/latest/setup.sh)"
```



如果需要使用华为云加速，可使用
```
CDN=1 bash -c "$(curl -fsSLk https://waf-ce.chaitin.cn/release/latest/setup.sh)"
```



如果需要安装最新版本流式检测模式，可使用
```
STREAM=1 bash -c "$(curl -fsSLk https://waf-ce.chaitin.cn/release/latest/setup.sh)"
```

![安装](https://img.picui.cn/free/2024/06/25/667a71b6a8361.jpg)

话不多说 这就来查看雷池新更新的动态防护吧
这里雷池的版本一定要在6.0版本以上哦
打开防护站点-站点管理-点击动态防护-启动开关
这样就打开动态防护啦
![waf](src\leichi_in.jpg)


可以在下面选择加密路径 这里我默认选择了主页站点

也可以添加其它需要保护的资源嗷

下面就来看下 没有加密的源代码是这样的

![未加密](src\open.jpg)

（简单打了个🐎hhhh
而开启了加密后 源代码是这样的

![加密](src\2.png)


会先进入一段加载页面

![演示](src\yanshi.png)


其实我挺希望这个解密时间能够再快一些，或者可以自定义一下这个页面之类的，每次进去都要五秒钟左右
后面就跳转到正常网页啦

### 想要体验的小伙伴们可以去官方DEMO体验
传送门: [点击访问官方DEMO](https://demo.waf-ce.chaitin.cn:9443/ "官方DEMO")
[点击体验动态防护](https://demo.waf-ce.chaitin.cn/ "动态防护体验")


有雷池的动态防护和WAF能力 感觉轻松多啦

![rt](src/alllllll.png)









