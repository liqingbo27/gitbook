# 配置

变量 |	描述
 -- | --
root |	包含所有图书文件的根文件夹的路径，除了 book.json
structure |	指定自述文件，摘要，词汇表等的路径，参考 Structure paragraph.
title |	您的书名，默认值是从 README 中提取出来的。在 GitBook.com 上，这个字段是预填的。
description |	您的书籍的描述，默认值是从 README 中提取出来的。在 GitBook.com 上，这个字段是预填的。
author |	作者名。在GitBook.com上，这个字段是预填的。
isbn |	国际标准书号 ISBN
language |	本书的语言类型 —— ISO code 。默认值是 en
direction |	文本阅读顺序。可以是 rtl （从右向左）或 ltr （从左向右），默认值依赖于 language | 的值。
gitbook |	应该使用的GitBook版本。使用 SemVer 规范，并接受类似于 “> = 3.0.0” 的条件。

##### root
包含所有图书文件的根文件夹的路径， book.json 文件除外。
例：
```
"root" : "./docs",
```
##### structure
指定 Readme、Summary、Glossary 和 Languages 对应的文件名。


##### title
电子书的书名，默认值是从 README 中提取出来的。在 GitBook.com 上，这个字段是预先填写的。
例：
```
"title" : "gitbook-notes",
```

##### author
作者姓名，在GitBook.com上，这个字段是预先填写的。
例：
```
"author" : "victor zhang"
```
##### description

电子书的描述，默认值是从 README 中提取出来的。在GitBook.com上，这个字段是预先填写的。

例：
```
"description" : "Gitbook 教程"
```
##### direction

文本的方向。可以是 rtl 或 ltr，默认值取决于语言的值。

例：
```
"direction" : "ltr"
```
##### gitbook

应该使用的GitBook版本。使用SemVer规范，接受类似于 >=3.0.0 的条件。

例：
```
"gitbook" : "3.0.0",
"gitbook" : ">=3.0.0"
```
##### language
Gitbook使用的语言, 版本2.6.4中可选的语言如下：
en, ar, bn, cs, de, en, es, fa, fi, fr, he, it, ja, ko, no, pl, pt, ro, ru, sv, uk, vi, zh-hans, zh-tw
例：
```
"language" : "zh-hans",
```
##### links
在左侧导航栏添加链接信息
例：
```
"links" : {
    "sidebar" : {
        "Home" : "https://github.com/dunwu/gitbook-notes"
    }
}
```

##### styles
自定义页面样式， 默认情况下各generator对应的css文件
例：
```
"styles": {
    "website": "styles/website.css",
    "ebook": "styles/ebook.css",
    "pdf": "styles/pdf.css",
    "mobi": "styles/mobi.css",
    "epub": "styles/epub.css"
}
```

例如要使 h1、h2 标签有下边框， 可以在 website.css 中设置
```
h1 , h2{
    border-bottom: 1px solid #EFEAEA;
}
```

###### plugins 插件列表
可以在插件前面加-符号删除默认插件，默认五种插件如下，更多插件
```
highlight：代码高亮
search：导航栏查询功能（不支持中文）
sharing：右上角分享功能
font-settings：字体设置（最上方的"A"符号）
livereload：为GitBook实时重新加载
pluginsConfig 配置插件的属性
```
### 参考：
```
{
    "title": "G笔记",
    "description": "好记性不如G笔记",
    "author": "lijiam",
    "output.name": "site",
    "language": "zh-hans",
    "gitbook": "3.2.3",
    "root": ".",
    "links": {
        "sidebar": {
            "首页": "http://www.lijiam.com"
        }
    },
    "plugins": [
        "code",
        "-search",
        "search-pro",
        "github",
        "splitter",
        "tbfed-pagefooter",
        "donate",
        "-sharing",
        "sharing-plus",
        "prism",
        "-highlight",
        "styles-less",
        "toggle-chapters",
        "multipart",
        "ancre-navigation"
    ],
    "pluginsConfig": {
        "github": {
            "url": "https://github.com/lijiam"
        },
        "code": {
            "copyButtons": true
        },
        "tbfed-pagefooter": {
            "copyright": "Copyright © lijiam 2019",
            "modify_label": "本书发布时间：",
            "modify_format": "YYYY-MM-DD HH:mm:ss"
        },
        "donate": {
            "wechat": "/assets/images/wxpay.png",
            "alipay": "/assets/images/alipay.png",
            "title": "",
            "button": "赏",
            "alipayText": "支付宝打赏",
            "wechatText": "微信打赏"
        },
        "sharing": {
            "facebook": true,
            "twitter": true,
            "weibo": true,
            "qq": true,
            "all": [
                "douban",
                "google",
                "qzone",
                "linkedin"
            ]
        },
        "prism": {
            "css": [
                "prismjs/themes/prism-solarizedlight.css"
            ],
            "lang": {
                "flow": "typescript"
            }
        }
    },
    "styles": {
        "website": "assets/styles/website.less",
        "ebook": "assets/styles/ebook.less",
        "pdf": "assets/styles/pdf.less",
        "mobi": "assets/styles/mobi.less",
        "epub": "assets/styles/epub.less"
    }
}
```