
# Express-Blog
新人学习使用nodejs的express框架搭建一个简单的博客，原地址是:<a href='https://github.com/nswbmw/N-blog'>N-blog</a>。 由于版本问题，遇到了一些坑：<a href='http://blog.csdn.net/xqnode/article/details/60663060'>nodejs小博客填坑指南</a>

#Express简介
Express是一个简洁而灵活的 node.js Web应用框架, 提供了一系列强大特性帮助你创建各种 Web 应用，和丰富的 HTTP 工具。

#技术领域：
- nodejs
- express
- Mongodb
- bootstrap

#开启项目方法：
安装git和nodejs。

下载源代码：

```
$ git clone https://github.com/RegToss/Express-Blog.git
```

进入代码目录，安装express-generator：

```
$ npm install -g express-generator
```
下载monodb数据库，在monodb根目录下新建文件夹blog用作数据库，
命令行模式下进入mongodb的根目录下的bin目录,设置数据库路径，并开启数据库：
```
$ cd bin
$ mongod --dbpath ../blog
```

接下来就可以运行代码了，进入源代码根目录，运行：
```
$ npm start
```

打开浏览器输入：localhost:3000查看效果。

下面是效果图：

##主页
默认登录和登出都会显示此页面，所有用户发表的博客都会在此集中显示

![主页.png](http://upload-images.jianshu.io/upload_images/4670483-8097fca6b9ff8dbd.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

##登录页
注册后的用户可以在此登录，只有登录才可以发表博客
![登录.png](http://upload-images.jianshu.io/upload_images/4670483-02fc7eb9ee7a703c.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


##注册页
注册成功的用户信息会写入数据库，这里使用的本地的数据库，所以看不到数据。可以在命令行或者客户端软件Robomongo中查看。
```
//切换到mogodb数据库的bin目录下运行
$ mongo 
$ use blog
$ db.users.find()
```

![注册.png](http://upload-images.jianshu.io/upload_images/4670483-8741929acbcf5c07.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

#发表博客页
登录后的用户可以在此写博文，点击提交后会将用户信息和博客信息存入mongodb数据库。主页将会显示最新的博文。

![发表.png](http://upload-images.jianshu.io/upload_images/4670483-6a49a99765af1c7c.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

#登出
登出后回到主页面，显示已发表的博客信息。

![登出.png](http://upload-images.jianshu.io/upload_images/4670483-60eacf7d2c344975.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

感谢您看完我的小作品，如果您对我有兴趣，请联系我，谢谢！<a href='http://regtoss.github.io'>我的简历</a>
