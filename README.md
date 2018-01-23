# Instructions_Jenkins_iOS
# Jenkins搭建iOS自动化打包测试使用说明

## 一. Jenkins安装
Jenkins在Mac上有两种安装方式。
> 参考[iOS持续集成：Jenkins篇](https://www.jianshu.com/p/faf879b3d182)

### 1. 	brew安装（推荐）:
安装环境要求：
> ①Java jdk8.x。测试中发现jdk版本高了也不行，在安装插件过程中会报错。如果Java版本不是8.x，则需要切换Java版本，参考：
> 
> [MAC JDK版本切换](http://www.cnblogs.com/maxinliang/p/4389971.html)    
> [MAC下安装多版本JDK和切换几种方式](http://chessman-126-com.iteye.com/blog/2162466)
> 
> ②brew

安装步骤：
> 安装 `$ brew install jenkins`
> 
> 安装之后启动 `jenkins`
> 
> 此时Jenkins会在命令行里打印相关的运行日志，再在浏览器里输入： http://localhost:8080/
> 
> 查看初始密码`$ sudo cat /Users/Shared/Jenkins/Home/secrets/initialAdminPassword`


更多指令：
> Jenkins启用 `$ sudo launchctl load /Library/LaunchDaemons/org.jenkins-ci.plist`
> 
> Jekins停用 `$ sudo launchctl unload /Library/LaunchDaemons/org.jenkins-ci.plist`



  


	
	
	
 
### 2.	Jenkins安装包安装[Jenkins官网](https://jenkins.io/)

## 二. Jenkins插件与配置
## 三. 常见问题
1. 在 ~/Library/Keychains 中找不到 login.keychain 文件

> Sierra 的问题。试试 ln -s ~/Library/Keychains/login.keychain-db ~/Library/Keychains/login.keychain

2. 邮件模板的文件路径需要自己建，默认本该存在但是实际不存在（如新建路径：.jenkins/email-templates/。邮件模板会自己去查找该路径）