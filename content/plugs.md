# 安装插件

在根目录下创建```book.json```文件

### 1、 配置

在```book.json```的```plugins```参数中添加插件名。
如：
```
{
    "plugins": ["mathjax"]
}
```


### 2、安装：

打开终端
```
gitbook install
```
或
```
npm install gitbook-plugin-插件名
```

### 3、重启服务或者重新打包

如果使用```gitbook install```安装的很慢，建议使用```npm init```初始化一个```package.json```文件，然后每个包通过npm命令安装，以后就可以通过npm install一键快速安装依赖包了。
#### 注意：
> 1、插件一定先要在book.json文件里面plugins中才能生效，如果只是安装了插件，而没配置的话是不会生效的。

> 2、gitbook命令安装慢，而且是全部插件都安装一遍，如果只安装一个插件的话建议使用NPM命令安装。

## 插件列表 plugins
配置使用的插件
```
"plugins": [
    "-search",
    "back-to-top-button",
    "expandable-chapters-small",
    "insert-logo"
]
```
其中```-search```中的 ```-``` 符号代表去除默认自带的插件

##### Gitbook默认自带有5个插件：
| 插件 | 说明 |
| -- | -- |
| highlight | 代码高亮 |
| search | 导航栏查询功能（不支持中文） |
| sharing | 右上角分享功能 |
| font-settings | 字体设置（最上方的"A"符号） |
| livereload | 为GitBook实时重新加载 |

## 插件属性配置pluginsConfig
配置插件的属性
例如配置insert-logo的属性：
```
  "pluginsConfig": {
    "insert-logo": {
      "url": "images/logo.png",
      "style": "background: none; max-height: 30px; min-height: 30px"
    }
  }
```
### 一些实用插件
记录一些实用的插件
用法：在book.json中添加"plugins"和"pluginConfig"字段。然后执行gitbook install，或者使用NPM安装npm install gitbook-plugin-插件名，也可以从源码GitHub地址中下载，放到node_modules文件夹里（GitHub地址在进入插件地址右侧的GitHub链接）
