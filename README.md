# wap.uestc.edu.cn

API of wap.uestc.edu.cn

wap.uestc.edu.cn的API分析文档

## index 首页

GET http://wap.uestc.edu.cn/api/index


| 字段    | 描述   | 长度   |
| ----- | ---- | ---- |
| info  | 通知   | 12   |
| slide | 展示栏  | 15   |
| news  | 新闻   | 8    |

```json

http://wap.uestc.edu.cn/api/index


{
    "info":[{
        "link":"/post/55939",
        "intro":"人力资源部教师发展中心开展“名师讲堂”系列活动，以定期邀请国内外知名专家学者、国家级教学名师等作专题报告，旨在加强广大师...",
        "title":"名师讲堂：Lightweight Cryptography for Internet-of-Things",
        "img":null
    }
    ......
    ],
    "news":[{
        "editor":["编辑：林坤","审核：罗莎","发布者："],
        "title":"学校举办第三届中山学院干部培训班",
        "sub_title":null,
        "link":"/post/55940",
        "img":["http://www.new1.uestc.edu.cn/upload/image/832bc907b6c22cd9761e9808de74f7b6.jpg","http://www.new1.uestc.edu.cn/upload/image/f1861c0aee53ed0e9deb1caa5cd456a5.jpg"],
        "content":"<div ......",
        "date":"2016-10-10",
        "authors":["文：杨丽可 图：文龙","来源：新闻中心","点击量：127"],
        "author":"文：杨丽可 图：文龙"
    }
    ......
    ],
    "slide":[{
        "link":"/post/55926",
        "intro":"10月8日上午，四川省人民政府与电子科技大学在成都签署战略合作协议。省委书记王东明，省委副书记、省长尹力，省委常委范锐平、吴...",
        "title":"四川省人民政府与电子科技大学签署战略合作协议",
        "img":"http://www.new1.uestc.edu.cn/upload/image/ea12353a90804bff0d4710110435107a.jpg"
    }
    ......
    ]
}

```

## colume 分类新闻

GET http://wap.uestc.edu.cn/api/column/{id}

一些字段的id

```js
e.menus = [{
        name: "焦点新闻",
        link: "/category/42"
    }, {
        name: "校园时讯",
        link: "/category/50"
    }, {
        name: "教育教学",
        link: "/category/43"
    }, {
        name: "科研学术",
        link: "/category/44"
    }, {
        name: "合作交流",
        link: "/category/45"
    }, {
        name: "信息公告",
        link: "/category/annoucement"
    }]

t.types = [{
        name: "学术",
        id: 66
    }, {
        name: "文化",
        id: 67
    }, {
        name: "公告",
        id: 68
    }]
```

```json
例如，教育教学
http://wap.uestc.edu.cn/api/column/43

[
    {
        "img": "http://www.new1.uestc.edu.cn/upload/image/e932acdc673e1cf0523f83051c568669.jpg",
        "intro": "8月25日至28日，RoboMasters2016全国大学生机器人大赛全国总决赛在深圳湾体育中心春茧体育馆点燃战火。电子科技大学One Point Five S战队凭借...",
        "link": "/post/55244",
        "title": "电子科大蝉联RoboMasters全国大学生机器人大赛总冠军"
    }
    ......
]
```


## p 单条新闻

GET http://wap.uestc.edu.cn/api/p/xxxx

```json
http://wap.uestc.edu.cn/api/p/55939

{
    "author": "文：教师发展中心",
    "authors": [
        "文：教师发展中心",
        "来源：人力资源部",
        "点击量：189"
    ],
    "content": "<div .....",
    "date": "2016-10-09",
    "editor": [
        "编辑：林坤",
        "审核：林坤",
        "发布者：林坤"
    ],
    "img": [],
    "sub_title": null,
    "title": "名师讲堂：Lightweight Cryptography for Internet-of-Things"
}


```

