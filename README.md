Heroku buildpack for Play framework
=========================

云帮play框架的项目的源码构建核心部分是基于[Heroku buildpack](https://github.com/heroku/heroku-buildpack-play) for [Play framework](http://www.playframework.org/)实现的。由于Play1.x版本不支持Scala语言，所以云帮支持的Play框架版本是基于Play2.x版本。

## 工作原理

如果您应用的源码已经符合buildpack识别Scala语言的标准，那么buildpack会继续检测您代码根目录的`/conf`目录下是否存在`application.conf`。若存在，您的代码将被识别为Play框架。

## 文档

以下文章了解更多：

- [云帮支持play框架](http://www.rainbond.com/docs/stable/user-lang-docs/scala/lang-scala-play.html)

## 配置

### 启动

云帮运行play框架时需要执行相关jar包，所以需要您创建`Procfile`文件，并输入以下内容： 

```bash
web: target/start $JAVA_OPTS
```

## 授权

根据 MIT 授权获得许可。 请参阅LICENSE文件
