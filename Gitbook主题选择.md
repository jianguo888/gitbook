# Gitbook主题选择

[https://www.npmjs.com/package/gitbook-plugin-theme-lou](https://www.npmjs.com/package/gitbook-plugin-theme-lou)



book.json文件

```text
{
  "title": "实验室",
  "description": "电子书教程",
  "author": "Breeze",
  "language": "zh-hans",
  "root": ".",
  "plugins": [
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
    "sharing-plus",
    "theme-lou"
  ],
  "styles": {
    "website": "styles/website.css"
  },
  "pluginsConfig": {
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
    },
    "theme-lou": {
      "color": "#FF4848",
      "favicon": "assets/favicon.ico",
      "logo": "assets/logo.png",
      "appleTouchIconPrecomposed152": "assets/avatar.png",
      "copyrightLogo": "assets/copyright.png",
      "forbidCopy": true,
      "search-placeholder": "输入关键字搜索",
      "book-summary-title": "文章目录",
      "book-anchor-title": "本章目录",
      "hide-elements": [
        ".summary .gitbook-link",
        ".summary .divider"
      ],
      "copyright": {
        "author": "breeze"
      }
    }
  },
  "variables": {
    "themeLou": {
      "nav": [
        {
          "target": "_blank",
          "url": "https://flutter.dev/",
          "name": "flutter官网"
        },
        {
          "target": "_blank",
          "url": "https://pub.flutter-io.cn/packages",
          "name": "插件"
        }
      ],
      "footer": {
        "donate": {
          "wechat": "https://luckly007.oss-cn-beijing.aliyuncs.com/img/image-20210922202901895.png",
          "wxpay": "https://luckly007.oss-cn-beijing.aliyuncs.com/img/image-20210922202901895.png",
          "alipay": "https://luckly007.oss-cn-beijing.aliyuncs.com/img/image-20210922202843746.png",
          "title": "『赠人玫瑰 🌹 手有余香 』",
          "avatar": "http://xkapp-uat.oss-cn-hangzhou.aliyuncs.com/2e7a3f70-80ab-4b50-93ec-a04dfeef949b/avatar-100.png",
          "nickname": "breeze",
          "button": "打赏",
          "alipayText": "支付宝",
          "wechatText": "微信",
          "message": "随意打赏，但不要超过一顿早餐钱 💕"
        }
      },
      "copyright": true
    }
  }
}
```

