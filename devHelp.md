To help develop , confirm the version and work.

## version

### local

​	main 8.17

### cloud

​	main  8.17



## dev

**to do**



**done**

- 编译运行成功 -~8.17     运行太占内存了，基本上占用3G，这样虚拟机就满了。


## problem

- **npm install**

**Q:**

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

**A:**

npm i --legacy-peer-deps 忽略此包的旧依赖项

- 启动项目时

**Q:**

org.springframework.beans.factory.UnsatisfiedDependencyException: Error creating bean with name 'sysConfigController': Unsatisfied dependency expressed through field 'configService'; nested exception is org.springframework.beans.factory.BeanCreationException: Error creating bean with name 'sysConfigServiceImpl': Invocation of init method failed; nested exception is org.apache.ibatis.binding.BindingException: Invalid bound statement (not found): com.ruoyi.system.mapper.SysConfigMapper.selectConfigList
	at org.springframework.beans.fact

**A:**

1. 配置nocas中的sql配置数据源，修改mysql账户密码
2. 配置redis

## help

[**环境部署**](http://doc.ruoyi.vip/ruoyi-cloud/document/hjbs.html#%E5%87%86%E5%A4%87%E5%B7%A5%E4%BD%9C)

**[Nacos 快速开始](https://nacos.io/zh-cn/docs/quick-start.html)**

bash startup.sh -m standalone

**[如何在 Ubuntu 20.04 上安装和配置 Redis](https://blog.csdn.net/snowdream86/article/details/106608928)**

sudo systemctl status redis-server

sudo systemctl restart redis-server

## study

**Shiro**

应用代码通过Subject来进行认证和授权，而Subject又委托给SecurityManager； 我们需要给Shrio的SecurityManager注入Realm，从而让SecurityManager能得到合法的用户及其权限进行判断，Shiro不提供维护用户/权限，而是通过Realm让开发人员自己注入。

Shiro不会去维护用户，维护权限；这些需要自己去设计/提供；然后通过响应的接口注入给Shiro即可
