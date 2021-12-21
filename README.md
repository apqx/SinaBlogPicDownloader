# SinaBlogPicDownloader

一个下载新浪博客里照片原图的下载器，根据博文URL解析出文章中所有缩略图对应的原图地址，批量下载。

参见[我的这篇文章](https://apqx.me/post/original/2021/12/12/关于-编程-的一件小事.html)。

```sh
java -jar SinaBlogPickDownload-x.y.z.jar
```

# v2.0.0

基于JDK 11，内置下载器，不再依赖Downie，可跨平台运行。

2种下载模式，下载目录为`[user]/Downlaod/sinaDownload/`。

1. 根据文章URL下载，自动解析URL，下载博文中所有的图片原图。
2. 根据缩略图下载，把想要的缩略图从浏览器拖到`[user]/Downlaod/sinaThumb/`中，执行此程序即可下载原图。

# v1.0.0

基于JDK 11，解析原图URL，把下载任务抛给Downie执行，因此只能在安装了Downie的macOS上运行。

2种下载模式，下载目录为`[user]/Downlaod/sinaDownload/`。

1. 根据文章URL下载，自动解析URL，下载博文中所有的图片原图。
2. 根据缩略图下载，把想要的缩略图从浏览器拖到`[user]/Downlaod/sinaThumb/`中，执行此程序即可下载原图。

因为Downie执行的一些限制，下载完成后需要执行一次合并。

3. 把下载的图片合并，格式化为以ID命名的jpg图片。