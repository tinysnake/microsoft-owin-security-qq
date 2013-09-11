Microsoft.Owin.Security.QQ
=================================

Middleware that enables an application to support [QQConnect](http://connect.qq.com/) OAuth 2.0 authentication workflow.

More information please visit: [Katana Project](http://katanaproject.codeplex.com/)

Please follow my weibo: [瘦不拉叽的SNAKE](http://weibo.com/tangfeifan) 

Install from nuget: 
`PM> Install-Package Microsoft.Owin.Security.QQ -Pre`([package url](https://www.nuget.org/packages/Microsoft.Owin.Security.QQ/0.1.0-rc2))

Or search `Microsoft.Owin.Security.QQ` in Nuget package manager, and make sure you selected the Include Prerelease selection of the filter dropdownlist.

这是一个使用QQ账号的第三方账户登录的owin中间件.

更多内容请访问: [Katana Project](http://katanaproject.codeplex.com/)

请关注我的微博: [瘦不拉叽的SNAKE](http://weibo.com/tangfeifan)

从Nuget中安装:

在Nuget控制台中输入: `Install-Package Microsoft.Owin.Security.QQ -Pre`([package网址](https://www.nuget.org/packages/Microsoft.Owin.Security.QQ/0.1.0-rc2))
或在Nuget的包管理器中搜索`Microsoft.Owin.Security.QQ`,并确保在包过滤的下拉菜单中选择Include Prerelease(包括预发行版)选项.
How to use:
===========

    //在你的"Startup"类的"Configure"方法中添加以下代码
    //别忘了添加Owin的命名空间.
    app.UseSinaWeiboAuthentication(
        appId: "your app id",
        appSecret: "your app secret");
        
一些小提示: 测试环境下请确保您的网站使用的是80端口,试图使用非80端口访问腾讯接口会有非法redirect_url错误.