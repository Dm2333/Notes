
# 账户生成

账户生成方案在本章节中主要分为两部分: 第三方平台账户体验以及客户端账户生成. 其中客户端账户生成又分为两个部分, 分别是账户注册与账户迁移. 其区别在于账户注册是针对许多在使用该客户端之前, 没有进行过账户体验或是曾经注册过账户的用户而言, 而账户迁移则关注的是进行过第三方账户体验, 或是曾经拥有过账户, 想要将以往的账户信息迁移到新创建的账户上的使用场景. 

----

## 第三方平台账户体验

为了方便用户对本体网络功能进行体验, 产生一个更为直观的印象. 我们将在支持auth功能的第三方社交平台上开发一些app程序, 用户可以使用这些app(如微信开发平台上的微信小程序)生成ont账户从而对本体网络进行初次体验, 其逻辑流程主要为: 
1. 用户在第三方平台上对app进行授权
1. app授权通过后得到的用户信息
1. app将会自动生成其ont账户及其密钥对. 
1. app通过用户信息对密钥对进行加密. 
1. 加密后的账户信息将被放置在app程序指定的云服务器上. 
1. 之后进行的任何加密, 签名, 验证等需要密钥对参与的操作, 都将会在用户每次授权之后, 查询并使用相应的密钥对完成指定操作.

----

##客户端账户生成



----

###账户注册



----

###账户迁移

由于本体网络的入口应用分为了运行在第三方开发平台上的app, 以及运行在用户本地空间的客户端程序. 因此账户迁移也分为两部分, 即从第三方平台app账户迁移到客户端账户和从客户端账户迁移到第三方平台app账户.

1. 当用户在第三方app完成体验并开始迁移到客户端程序时, 其逻辑流程主要如下:

    1. 设置客户端口令生成一份密钥对K_a. 
    1. 通过第三方平台授权客户端获得用户信息
    1. 通过用户信息获取到云服务器上的账户信息
    1. 使用云服务器中的账户信息将新密钥对K_a添加到该ont账户上.

1. 用户从客户端程序迁移到第三方app的流程与上面类似:

    1. 通过第三方授权生成一份密钥对K_b
    1. 在第三方app中输入客户端口令(或其他登录认证方式)
    1. 通过口令获取到ont账户信息
    1. 将新密钥对K_b添加到该ont账户上.




