---
title: 李星星github个人博客搭建过程
date: 2016-10-26 23:26:37
tags:
---
## 一、准备软件
依次下载一下软件即可（过程略）

>* [node.js](https://nodejs.org/en/)
* [Git](http://git-scm.com/)

## 二、配置SSH Keys
首先我们需要检查你电脑上现有的ssh key：

```jacascript
$ cd .ssh
```

如果提示：No such file or directory 说明你是第一次使用git。

## 三、生成新的SSH Key：
```jacascript
$ ssh-keygen -t rsa -C "邮件地址@youremail.com"
```
注意1: 此处的邮箱地址，你可以输入自己的邮箱地址；注意2: 此处的「-C」的是大写的「C」
```jacascript
Generating public/private rsa key pair.
Enter file in which to save the key (/Users/your_user_directory/.ssh/id_rsa):<回车就好>
```
然后系统会要你输入密码：**注意输入密码时不会显示任何东西**
```jacascript
Enter passphrase (empty for no passphrase):<输入加密串>
Enter same passphrase again:<再次输入加密串>
```
## 四、添加SSH Keys到github

在本机设置SSH Key之后，需要添加到GitHub上，以完成SSH链接的设置。

1、按照git中的目录打开本地id_rsa.pub文件。此文件里面内容为刚才生成的密钥。如果看不到这个文件，你需要设置显示隐藏文件。准确的复制这个文件的内容，才能保证设置的成功。

2、登陆github系统。点击头像--->**settings** ---> 左侧**SSH and GPG keys**--->**New SSH key**

3、把你本地生成的密钥复制到里面（key文本框中）， 点击 add key 就ok了

## 五、克隆网站到本地

```jacascript
$ git clone https://github.com/daohehu/daohehu.github.io.git
```
## 六、总结
到此我就把以前和李笑来老师学习建设的github网页下载到本地了，这篇教程是根据CNFeat的教程再根据自己在实践过程中遇到的不同而重新整理的。

如果需要完整教程请看这里[《如何搭建一个独立博客——简明Github Pages与Hexo教程》](http://www.jianshu.com/p/05289a4bc8b2)

## 【附录】
命令符收集:不知道有没有用先记下来吧。
>  版本信息查看：`git --version` `npm --version`
