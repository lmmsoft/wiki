# 抓取信息相关内容

## mercury-parser-api
- 源码 https://github.com/postlight/parser-api
- 介绍页 https://reader.postlight.com/
- 包装成的容器: https://github.com/HenryQW/mercury-parser-api
- AWS Lambda-based API
```
curl localhost:3000/parser?url=https://www.bbc.co.uk/news/science-environment-35876621

Response
{
    "title": "Ash tree set for extinction in Europe",
    "author": "Claire Marshall BBC Environment Correspondent",
    "date_published": null,
    "dek": null,
    "lead_image_url": "https://ichef.bbci.co.uk/news/1024/branded_news/9736/production/_88901783_88901782.jpg",
    "content": "<div><p class=\"byline\"> <span class=\"byline__name\">By Claire Marshall</span> <span class=\"byline__title\">BBC Environment Correspondent</span> </p><div class=\"story-body__inner\"> <figure class=\"media-landscape has-caption full-width lead\"> <span class=\"image-and-copyright-container\"> <img class=\"js-image-replace\" alt=\"Ash tree with suspected dieback\" src=\"https://ichef.bbci.co.uk/news/320/cpsprodpb/9736/production/_88901783_88901782.jpg\" width=\"976\"> <span class=\"off-screen\">Image copyright</span> <span class=\"story-image-copyright\">PA</span> </span> <figcaption class=\"media-caption\"> <span class=\"off-screen\">Image caption</span> <span class=\"media-caption__text\"> The chalara dieback has devastated ash trees across Europe </span> </figcaption> </figure><p class=\"story-body__introduction\">The ash tree is likely to be wiped out in Europe, according to a review of the evidence.</p><p>The trees are being killed off by the fungal disease ash-dieback along with an invasive beetle called the emerald ash borer.</p><p>According to the research, published in the Journal of Ecology, the British countryside will never look the same again.</p><p>The paper says that the ash will most likely be &quot;eliminated&quot; in Europe.</p><p>This could mirror the way Dutch elm disease largely wiped out the elm in the 1980s.</p><p><a href=\"http://www.bbc.co.uk/news/science-environment-33744042\" class=\"story-body__link\">Warning over ash dieback disease</a></p><p><a href=\"/news/uk-northern-ireland-33480275\" class=\"story-body__link\">100,000 trees destroyed over disease</a></p><p><a href=\"http://www.bbc.co.uk/news/science-environment-20171524\" class=\"story-body__link\">How to spot ash dieback</a></p><p>Ash trees are a key part of the treescape of Britain. You don&apos;t have to go to the countryside to see them. In and around towns and cities there are 2.2 million. In woodland, only the oak is more common.</p><p>However, according to a review led by Dr Peter Thomas of Keele University and published in the Journal of Ecology, &quot;between the fungal disease ash dieback and a bright green beetle called the emerald ash borer, it is likely that almost all ash trees in Europe will be wiped out - just as the elm was largely eliminated by Dutch elm disease&quot;.</p><p>Ash dieback, also known as Chalara, is a disease that was first seen in Eastern Europe in 1992. It now affects more than 2 million sq km, from Scandinavia to Italy.</p><figure class=\"media-landscape no-caption full-width\"> </figure><figure class=\"media-landscape has-caption full-width\"> <div class=\"image-and-copyright-container\"> <span class=\"off-screen\">Image copyright</span> <span class=\"story-image-copyright\">Getty Images</span> </div> <figcaption class=\"media-caption\"> <span class=\"off-screen\">Image caption</span> <span class=\"media-caption__text\"> The loss of ash trees won&apos;t just change the landscape, it will have a severe impact on biodiversity </span> </figcaption> </figure><p>It was identified in England in 2012 in a consignment of imported infected trees. It has since spread from Norfolk and Suffolk to South Wales. Caused by the fungus <i>Hymenoscyphus fraxineus</i>, it kills the leaves, then the branches, trunk and eventually the whole tree. It has the potential to destroy 95% of ash trees in the UK.</p><p>The emerald ash borer is a bright green beetle that, like ash dieback, is native to Asia. It&apos;s not yet in the UK but is spreading west from Moscow at a rate of 25 miles (41 km) a year and is thought to have reached Sweden.</p><p>The adult beetles feed on ash trees and cause little damage. However the larvae bore under the bark and in to the wood, killing the tree.</p><p>According to Dr Thomas: &quot;Our European ash is very susceptible to the beetle. It is only a matter of time before it spreads across the rest of Europe - including Britain - and the beetle is set to become the biggest threat faced by ash in Europe, potentially far more serious than ash dieback.&quot;</p><figure class=\"media-landscape has-caption full-width\"> <div class=\"image-and-copyright-container\"> <span class=\"off-screen\">Image copyright</span> <span class=\"story-image-copyright\">Science Photo Library</span> </div> <figcaption class=\"media-caption\"> <span class=\"off-screen\">Image caption</span> <span class=\"media-caption__text\"> The emerald ash borer also threatens ash trees </span> </figcaption> </figure><p>This won&apos;t just change our landscape - it will have a severe impact on biodiversity. 1,000 species are associated with ash or ash woodland, including 12 types of bird, 55 mammals and 239 invertebrates.</p><p>Mr Thomas said, &quot;Of these, over 100 species of lichens, fungi and insects are dependent upon the ash tree and are likely to decline or become extinct if the ash was gone.</p><p>&quot;Some other trees such as alder, small-leaved lime and rowan can provide homes for some of these species... but if the ash went, the British countryside would never look the same again.&quot;</p><p>One small hope is that some cloned ash trees have shown resistance against the fungus. But that won&apos;t protect them against the beetle.</p><p>Follow Claire <a href=\"http://twitter.com/bbcmarshall\" class=\"story-body__link-external\">on Twitter.</a></p> </div></div>",
    "next_page_url": null,
    "url": "https://www.bbc.co.uk/news/science-environment-35876621",
    "domain": "www.bbc.co.uk",
    "excerpt": "The ash tree is likely to be wiped out in Europe, according to the largest-ever survey of the species.",
    "word_count": 585,
    "direction": "ltr",
    "total_pages": 1,
    "rendered_pages": 1
}
```

```
http://xxx:3000/parser?url=%20http://www.baidu.com/

{
"title": "百度一下，你就知道",
"author": null,
"date_published": null,
"dek": null,
"lead_image_url": null,
"content": "<div id=\"s-user-setting-menu\" class=\"s-top-userset-menu c-floating-box c-font-normal \"><a class=\"s-set-hotsearch set-hide\" href=\"javascript:;\">&#x5173;&#x95ED;&#x70ED;&#x641C;</a><a class=\"s-set-hotsearch set-show\" href=\"javascript:;\">&#x5F00;&#x542F;&#x70ED;&#x641C;</a></div>",
"next_page_url": null,
"url": " http://www.baidu.com/",
"domain": "www.baidu.com",
"excerpt": "关闭热搜开启热搜",
"word_count": 2,
"direction": "ltr",
"total_pages": 1,
"rendered_pages": 1
}
```

```
curl 0.0.0.0:3000

{"message":"Welcome to 🚀mercury-parser-api API! Endpoint: /parser"}
```

抓公众号效果很好，还能刚拿到复杂的文章链接。配合 html_to_md 工具，转成的 markdown 也是很好的， 比如 https://codebeautify.org/html-to-markdown
```
http://xxx:3000/parser?url=https://mp.weixin.qq.com/s/yK5iW21wBpWRu5sWfgFycA

{
"title": "换行与跨界",
"author": null,
"date_published": null,
"dek": null,
"lead_image_url": "https://mmbiz.qpic.cn/mmbiz_jpg/FvfOcicboXakUxc4chSYQ7VDjQgddmhrJQ0x2ibLl2U5n7c4foaB7hI51gicw8p4E1OvjVbiaA3C2oYK7DnSXek8pQ/0?wx_fmt=jpeg",
"content": "<div id=\"img-content\" class=\"rich_media_wrp\">xxxx .. xxxx</div>",
"next_page_url": null,
"url": "http://mp.weixin.qq.com/s?__biz=MzU3MjYzNTkyMQ==&mid=2247484837&idx=1&sn=29dba676e706e865edc4b8851b819b2f&chksm=fcccabdbcbbb22cd5248b8818b87b7d687bda72eb5456c461136f8871bf37bdbbba3c4a9217e#rd",
"domain": "mp.weixin.qq.com",
"excerpt": "主动布局，文理兼修，是换行与跨界的关键要素",
"word_count": 32,
"direction": "ltr",
"total_pages": 1,
"rendered_pages": 1
}
```
