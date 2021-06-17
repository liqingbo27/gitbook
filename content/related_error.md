# 相关错误

#### 编译报错gitbook\gitbook-plugin-fontsettings\fontsettings.js
gitbook build命令运行包错，具体如下：


![编译报错gitbook](/images/related_error/微信截图_20200407144720.png "编译报错gitbook\gitbook-plugin-fontsettings\fontsettings.js")

找到当前文件 ```copyPluginAssets.js```
```
C:\Users\32631\.gitbook\versions\3.2.3\lib\output\website
```
112行
和
67行

> 解决方案：注释掉112行和67行或者改为false

如图：


![编译报错gitbook](/images/related_error/微信截图_20200407144930.png "编译报错gitbook\gitbook-plugin-fontsettings\fontsettings.js")

![编译报错gitbook](/images/related_error/微信截图_20200407144957.png "编译报错gitbook\gitbook-plugin-fontsettings\fontsettings.js")



