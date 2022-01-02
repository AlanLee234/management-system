To help develop , confirm the version and work.

## version

### local

​	main 1.2

### cloud

​	main  1.2



## dev

**to do**



**done**

- 编译运行成功 -~8.17     运行太占内存了，基本上占用3G，这样虚拟机就满了。

  

## problem

**Q：**微服务占内存和空间这么大，为什么要引入呢？实际开发中真的会为方便性，这么耗费系统的资源？

**A：**网上的解决方案是调java的jvm，即内存占用

**Q: 启动项目时**

org.springframework.beans.factory.UnsatisfiedDependencyException: Error creating bean with name 'sysConfigController': Unsatisfied dependency expressed through field 'configService'; nested exception is org.springframework.beans.factory.BeanCreationException: Error creating bean with name 'sysConfigServiceImpl': Invocation of init method failed; nested exception is org.apache.ibatis.binding.BindingException: Invalid bound statement (not found): com.ruoyi.system.mapper.SysConfigMapper.selectConfigList
	at org.springframework.beans.fact

**A:**

1. 配置nocas中的sql配置数据源，修改mysql账户密码

2. 配置redis，并启动  sudo /etc/init.d/redis-server start 	https://www.cnblogs.com/viaivi/archive/2011/12/08/2281319.html

   

**Q: npm install**

While resolving: ruoyi@3.0.0
Found: webpack@5.42.1
node_modules/webpack
  peer webpack@"^4.0.0 || ^5.0.0" from html-webpack-plugin@4.5.2
  node_modules/html-webpack-plugin
    peer html-webpack-plugin@"^3.0.0 || ^4.0.0" from script-ext-html-webpack-plugin@2.1.5
    node_modules/script-ext-html-webpack-plugin
      dev script-ext-html-webpack-plugin@"2.1.5" from the root project

Could not resolve dependency:
peer webpack@"^1.0.0 || ^2.0.0 || ^3.0.0 || ^4.0.0" from script-ext-html-webpack-plugin@2.1.5
node_modules/script-ext-html-webpack-plugin
  dev script-ext-html-webpack-plugin@"2.1.5" from the root project

**A:**  npm i --legacy-peer-deps  忽略此包的旧依赖项



## help

RuoYiGatewayApplication （网关模块 必须）
RuoYiAuthApplication （认证模块 必须）
RuoYiSystemApplication （系统模块 必须）

**网址**

[项目前端页面](http://localhost:1024/login?redirect=%2Fsystem%2Fuser)

[项目文档](http://doc.ruoyi.vip/ruoyi-cloud/document/qdsc.html#%E9%80%9A%E7%94%A8%E6%96%B9%E6%B3%95)

[项目源码](https://gitee.com/y_project/RuoYi-Cloud)

[nocoa guide](https://nacos.io/zh-cn/docs/what-is-nacos.html)



[**环境部署**](http://doc.ruoyi.vip/ruoyi-cloud/document/hjbs.html#%E5%87%86%E5%A4%87%E5%B7%A5%E4%BD%9C)

**[Nacos 快速开始](https://nacos.io/zh-cn/docs/quick-start.html)**

​	bash startup.sh -m standalone

​	sh shutdown.sh

​	启动后访问 http://192.168.152.128:8848/nacos/index.html

**[如何在 Ubuntu 20.04 上安装和配置 Redis](https://blog.csdn.net/snowdream86/article/details/106608928)**

​	sudo systemctl status redis-server

​	sudo systemctl restart redis-server

[Mock](https://github.com/nuysoft/Mock/wiki)

mockjs的原理是:拦截了所有的请求并代理到本地模拟数据，所以 network 中没有任何的请求发出

[Element](https://element.eleme.cn/#/zh-CN/component/installation)



## study

**Shiro**

应用代码通过Subject来进行认证和授权，而Subject又委托给SecurityManager； 我们需要给Shrio的SecurityManager注入Realm，从而让SecurityManager能得到合法的用户及其权限进行判断，Shiro不提供维护用户/权限，而是通过Realm让开发人员自己注入。

Shiro不会去维护用户，维护权限；这些需要自己去设计/提供；然后通过响应的接口注入给Shiro即可

**页面权限**
有很多人表示他们公司的路由表是于后端根据用户的权限动态生成的，我司不采取这种方式的原因如下：
项目不断的迭代你会异常痛苦，前端新开发一个页面还要让后端配一下路由和权限，让我们想了曾经前后端不分离，被后端支配的那段恐怖时间了。
