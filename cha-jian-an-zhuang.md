# 插件安装

book.json，该文件用于存放配置信息。

【title】书本的标题 【author】作者的相关信息 【description】本书的简单描述 【language】gitbook使用的语言 【root】指定存放 GitBook 文件（除了 book.json）的根目录 【structure】指定自述文件，摘要，词汇表等的路径

gitbook支持许多插件，可以扩展gitbook的功能。

参考本人完整配置详情：

```text
{
    "title": "信息系统项目管理师",
    "description": "信息系统项目管理师电子书教程",
    "author": "Breeze",
    "language": "zh-hans",
    "root": ".",
    "plugins": [
        "donate",
        "github-buttons@2.1.0",
        "edit-link",
        "splitter",
        "tbfed-pagefooter",
        "expandable-chapters",
        "back-to-top-button",
        "code",
        "pageview-count",
        "popup",
        "search-plus",
        "-lunr",
        "-search",
        "splitter",
        "-sharing",
        "sharing-plus"
    ],
    "styles": {
        "website": "styles/website.css"
    },
    "pluginsConfig": {
        "donate": {
            "wechat": "https://luckly007.oss-cn-beijing.aliyuncs.com/img/image-20210922202901895.png",
            "alipay": "https://luckly007.oss-cn-beijing.aliyuncs.com/img/image-20210922202843746.png",
            "title": "",
            "button": "打赏",
            "alipayText": "支付宝",
            "wechatText": "微信"
        },
        "github-buttons": {
            "repo": "ITmxs/gitbook-Information-System-Engineer",
            "types": [
                "star"
            ],
            "size": "small"
        },
        "edit-link": {
            "base": "https://github.com/ITmxs/gitbook-Information-System-Engineer/edit/master",
            "label": "Edit This Page"
        },
        "tbfed-pagefooter": {
            "copyright": "&copy luckly FED Team",
            "modify_label": "该文件修订时间：",
            "modify_format": "YYYY-MM-DD HH:mm:ss"
        },
        "pluginsConfig": {
            "expandable-chapters": {}
        },
        "sharing": {
            "douban": false,
            "facebook": false,
            "google": false,
            "pocket": false,
            "qq": false,
            "qzone": false,
            "twitter": false,
            "weibo": false,
            "all": [
                "qq",
                "qzone",
                "viber",
                "whatsapp",
                "douban",
                "facebook",
                "google",
                "instapaper",
                "linkedin",
                "messenger",
                "twitter",
                "weibo"
            ]
        }
    }
}
```

## 记得运行 

```text
gitbook install
```

## 插件说明

【目录章节可折叠：expandable-chapters】

```text
{
    {
        plugins: ["expandable-chapters"]
    }
    {
        "pluginsConfig": {
            "expandable-chapters":{}
        }
    }
}
```

【畅言评论：changyan】

```text
{
    "plugins": [
        "changyan"
    ],
    "pluginsConfig": {
        "changyan": {
            "appid": "your changyan's appid",
            "conf": "the conf in the code generate by changyan"
        }
    }
}
```



编辑“book.json”文件，添加如下代码：

```text
{
    "styles": {
        "website": "styles/website.css"
    }
}
```



### page-treeview 目录

[GitHub 地址](https://github.com/aleen42/gitbook-treeview)

不需要在文档中插入标签，能够支持到 6 级目录，安装即可用。 这个插件生成目录以后，下面有一行关于版权的文字。 这行文字可以通过样式来进行控制，让它不显示出来。

```text
.treeview__container {
    margin-bottom: 0px !important;
}
.treeview__container-title {
    display: none !important;
}
```

### code 代码

[GitHub 地址](https://github.com/TGhoul/gitbook-plugin-code)

为代码块添加行号和复制按钮，复制按钮可关闭 单行代码无行号。

```text
"code": {
        "copyButtons": false
      }
```

### pageview-count 阅读量计数

该插件用来统计当前页面被访问次数

### popup 图片点击查看

[GitHub 地址](https://github.com/somax/gitbook-plugin-popup)

插件用于点击图片时，打开新的网页用来查看高清大图。

### tbfed-pagefooter 页面添加页脚（简单版）

[GitHub 地址](https://github.com/zhj3618/gitbook-plugin-tbfed-pagefooter)

在每个页面的最下方自动添加页脚信息，配置如下：

```text
"tbfed-pagefooter": {
            "copyright": "Copyright © levywang123@gmail.com 2020",
            "modify_label": "该文章修订时间：",
            "modify_format": "YYYY-MM-DD HH:mm:ss"
        },
```

### page-copyright 页面添加页脚（复杂版）

[GitHub 地址](https://github.com/skyFi/gitbook-plugin-page-footer)

在每个页面的最下方自动添加页脚配置的各个信息，配置如下：

```text
 "page-copyright": {
          "description": "footer",
          "copyright": "Copyright © levywang123@gmail.com 2020",
          "timeColor": "#ccc",
          "copyrightColor": "#ddd",
          "utcOffset": "8",
          "style": "normal",
          "noPowered": false,
          "signature": "levy",
          "wisdom": "footer",
          "format": "YYYY-MM-dd hh:mm:ss",
        },
```

### favicon 修改图标

修改网页标题的图标，显示个性化 ico

```text
        "favicon": {
            "shortcut": "assets/favicon.ico",
            "bookmark": "assets/favicon.ico",
            "appleTouch": "assets/favicon.ico",
            "appleTouchMore": {
                "120x120": "assets/favicon.ico",
                "180x180": "assets/favicon.ico"
            }
        },
```

### search-plus 替换原搜索插件

原搜索插件不支持中文搜索，所以使用该插件进行替换。需要将原插件进行去除掉。

```text
    "plugins": [ "search-plus", "-lunr", "-search"]
```

### expandable-chapters 及 chapter-fold 导航目录

两个插件配合使用，使导航目录使用更正常，以免出现导航栏问题。

一个支持多层目录，一个是在目录前方加上箭头。使点击两个都有效。

### hide-element 隐藏界面元素

[GitHub 地址](https://github.com/gonjay/gitbook-plugin-hide-element)

可以隐藏不想看到的元素，比如导航栏中 下方的 `Published by GitBook`

```text
"elements": [".gitbook-link"]
```

### back-to-top-button 返回顶部

[GitHub 地址](https://github.com/stuebersystems/gitbook-plugin-back-to-top-button)

在页面篇幅过长时，在界面右下角自动添加上返回顶部的按钮。

### splitter 侧边栏宽度调整

[GitHub 地址](https://github.com/yoshidax/gitbook-plugin-splitter)

添加完插件后，在界面上 侧边栏可自行调整宽度。

### sharing-plus 分享插件

[插件地址](https://plugins.gitbook.com/plugin/sharing-plus)

需要将自带的插件给隐藏掉 `-sharing` 分享当前页面，比默认的 sharing 插件多了一些分享方式。

```text
"sharing": {
             "douban": false,
             "facebook": false,
             "google": false,
             "pocket": false,
             "qq": false,
             "qzone": false,
             "twitter": false,
             "weibo": false,
          "all": [
              "qq", "qzone","viber","whatsapp",
               "douban", "facebook", "google", "instapaper", "linkedin",
               "messenger","twitter", "weibo"
           ]
       }
```

### 

