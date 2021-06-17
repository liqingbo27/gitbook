# 安装 GitBook
输入下面的命令来安装 GitBook。
```
$ npm install gitbook-cli -g
```
安装完成之后，你可以使用下面的命令来检验是否安装成功。

```
$ gitbook -V
CLI version: 2.3.2
GitBook version: 3.2.3
```


## 1.初始化
打开一个文件夹 MyGitBook
使用 gitbook init 初始化文件夹，会自动生成两个必要的文件 ```README.md``` 和 ```SUMMARY.md```
```
$ gitbook init
```

| 文件 | 说明 |
| -- | -- |
| README.md | 书的介绍文字，如前言、简介，在章节中也可做为章节的简介。  |
| SUMMARY.md | 定制书籍的章节结构和顺序。   |

```README.md``` 和 ```SUMMARY.md``` 是 **GitBook** 制作电子书的必要文件

## 2.预览
方式一：
```
gitbook serve
```

gitbook 会启动一个 4000 端口用于预览。

方式二：
```
gitbook build
```

生成.html静态文件，配置后可以直接访问预览
