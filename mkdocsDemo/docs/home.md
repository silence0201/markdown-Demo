# 首页接口

## 首页导航栏搜索接口

- 请求方式：GET

- 请求地址：/search/suggest/homepage_suggest/？

- 请求参数

| 参数         | 类型     | 是否必须 | 描述 | 示例   |
| --------- | ------ | :--: | ------- | ------------- |
| device_id | Int    |  N   | 设备 ID   | 8800803362  |
| iid      | Int    |  N   | 未知      | 14486549076 |

返回数据
```
{
    "message": "success",
    "data": {
        "call_per_refresh": 2,
        "homepage_search_suggest": "左手右手手表 | 一个西瓜 | 人人都是产品经理"
    }
}
```

## 首页顶部标题接口

- 请求方式：GET

- 请求地址：/article/category/get_subscribed/v1/?

- 请求参数

| 参数             | 类型   | 是否必须 | 描述   | 示例           |
| --------------- | ------ | :--: | ------- | ---------------|
| device_id       | Int    |  N   | 设备 ID  | 8800803362     |
| iid             | Int    |  N   | 未知     | 14486549076    |

返回数据示例：

```
{
    "message": "success",
    "data": {
        "version": "0",
        "data": [
            {
                "category": "news_hot",
                "web_url": "",
                "flags": 0,
                "name": "热点",
                "tip_new": 0,
                "default_add": 1,
                "concern_id": "",
                "type": 4,
                "icon_url": ""
            },
            {
                "category": "video",
                "web_url": "",
                "flags": 0,
                "name": "视频",
                "tip_new": 0,
                "default_add": 1,
                "concern_id": "",
                "type": 4,
                "icon_url": ""
            }
            // ...
        ]
    }
}
```

## 首页新闻列表数据接口

- 请求方式：GET

- 请求地址 1：/api/news/feed/v58/?
- 请求地址 2：/api/news/feed/v64/?（也是视频列表接口）
- 请求地址 2：/api/news/feed/v68/?
- 请求地址 2：/api/news/feed/v75/?

- 请求参数

| 参数        | 类型     | 是否必须 | 描述    | 示例         |
| --------- | ------ | ---- | ----- | ---------- |
| device_id | Int    | N    | 设备 ID | 8800803362 |
| category  | String | N    | 新闻类别  | video   |
| tt_from  | String | N    | 下拉刷新或加载更多  | pull / load_more  |
| refresh_reason  | Int | N    |   | 1  |
| strict  | Int | N    |   | 0  |
| detail  | Int | N    |   | 1  |
| min_behot_time  | Int | 下拉刷新的参数   |   | 1515848500  |
| max_behot_time  | Int | 加载更多的参数   |   | 1515848500  |

> 和视频列表数据接口相同， category 为 video

返回数据有如下几种情况：

### 推荐

#### 1.无图

返回的数据：
```
{
    "abstract":"新华社厦门9月6日电 题：开启新的金砖合作发展之门——习近平主席出席金砖国家领导人厦门会晤系列活动纪实“我衷心希望厦门会晤为我们开启新的合作之门、发展之门，迎来金砖合作第二个‘金色十年’，开辟新兴市场国家和发展中国家光明未来。”——习近平厦庇五洲客，门纳万顷涛。",
    "action_list":[
        {
            "action":1,
            "desc":"",
            "extra":{

            }
        }
    ],
    "aggr_type":1,
    "allow_download":false,
    "article_alt_url":"http://toutiao.com/group/article/6462594562829140237/",
    "article_sub_type":0,
    "article_type":1,
    "article_url":"http://news.xinhuanet.com/world/2017-09/06/c_1121617232.htm",
    "ban_comment":0,
    "behot_time":1504772050,
    "bury_count":0,
    "cell_flag":11,
    "cell_layout_style":1,
    "cell_type":0,
    "comment_count":96,
    "cursor":1504772050999,
    "digg_count":7,
    "display_url":"http://toutiao.com/group/6462594562829140237/",
    "forward_info":{
        "forward_count":21
    },
    "group_id":6462594562829140000,
    "has_m3u8_video":false,
    "has_mp4_video":0,
    "has_video":false,
    "hot":0,
    "ignore_web_transform":1,
    "is_stick":true,
    "is_subject":false,
    "item_id":6462602027422713000,
    "item_version":0,
    "keywords":"金砖国家领导人,厦门,习近平主席,金砖国家,国际会议中心",
    "label":"置顶",
    "label_style":1,
    "level":0,
    "like_count":7,
    "log_pb":{
        "impr_id":"20170907161410010008017131695F0E"
    },
    "media_info":{
        "avatar_url":"http://p2.pstatp.com/large/3658/7378365093",
        "follow":false,
        "is_star_user":false,
        "media_id":4377795668,
        "name":"新华网",
        "recommend_reason":"",
        "recommend_type":0,
        "user_id":4377795668,
        "user_verified":true,
        "verified_content":""
    },
    "media_name":"新华网",
    "preload_web":1,
    "publish_time":1504690890,
    "read_count":934864,
    "repin_count":10094,
    "rid":"20170907161410010008017131695F0E",
    "share_count":2600,
    "share_url":"http://toutiao.com/group/6462594562829140237/?iid=14462706438&app=news_article",
    "show_portrait":false,
    "show_portrait_article":false,
    "source":"新华网",
    "source_icon_style":1,
    "source_open_url":"sslocal://profile?uid=4377795668",
    "stick_label":"置顶",
    "stick_style":1,
    "tag":"news_politics",
    "tag_id":6462594562829140000,
    "tip":0,
    "title":"习近平出席金砖国家领导人厦门会晤系列活动纪实",
    "ugc_recommend":{
        "activity":"",
        "reason":"新华网官方头条号"
    },
    "url":"http://news.xinhuanet.com/world/2017-09/06/c_1121617232.htm",
    "user_info":{
        "avatar_url":"http://p3.pstatp.com/thumb/3658/7378365093",
        "description":"传播中国，报道世界；权威声音，亲切表达。",
        "follow":false,
        "follower_count":0,
        "name":"新华网",
        "user_auth_info":{
            "auth_type":"0",
            "auth_info":"新华网官方头条号"
        },
        "user_id":4377795668,
        "user_verified":true,
        "verified_content":"新华网官方头条号"
    },
    "user_repin":0,
    "user_verified":1,
    "verified_content":"新华网官方头条号",
    "video_style":0
}
```

#### 2.一大图


返回的数据：
```
{
    "abstract":"",
    "action_extra":{
        "channel_id":5443492141
    },
    "action_list":[
        {
            "action":1,
            "desc":"",
            "extra":{

            }
        },
        {
            "action":3,
            "desc":"",
            "extra":{

            }
        },
        {
            "action":7,
            "desc":"",
            "extra":{

            }
        },
        {
            "action":9,
            "desc":"",
            "extra":{

            }
        }
    ],
    "aggr_type":1,
    "allow_download":false,
    "article_sub_type":0,
    "article_type":0,
    "article_url":"http://toutiao.com/group/6448485086420697357/",
    "ban_comment":0,
    "behot_time":1503489767,
    "bury_count":0,
    "cell_flag":11,
    "cell_layout_style":1,
    "cell_type":0,
    "comment_count":4,
    "cursor":1503489767999,
    "digg_count":1,
    "display_url":"http://toutiao.com/group/6448485086420697357/",
    "filter_words":[
        {
            "id":"8:0",
            "is_selected":false,
            "name":"看过了"
        },
        {
            "id":"7:6",
            "is_selected":false,
            "name":"标题党"
        },
        {
            "id":"5:1469309637",
            "is_selected":false,
            "name":"拉黑作者:云端之战"
        },
        {
            "id":"2:11781250",
            "is_selected":false,
            "name":"不想看:手机"
        },
        {
            "id":"6:18151",
            "is_selected":false,
            "name":"不想看:iphone"
        }
    ],
    "forward_info":{
        "forward_count":0
    },
    "gallary_flag":1,
    "gallary_image_count":5,
    "group_flags":131072,
    "group_id":6448485086420697000,
    "has_image":true,
    "has_m3u8_video":false,
    "has_mp4_video":0,
    "has_video":false,
    "hot":0,
    "ignore_web_transform":0,
    "image_list":[
        {
            "height":438,
            "uri":"list/640x360/31d2000192851c1c56b2",
            "url":"http://p3.pstatp.com/list/640x360/31d2000192851c1c56b2",
            "url_list":[
                {
                    "url":"http://p3.pstatp.com/list/640x360/31d2000192851c1c56b2"
                },
                {
                    "url":"http://pb9.pstatp.com/list/640x360/31d2000192851c1c56b2"
                },
                {
                    "url":"http://pb1.pstatp.com/list/640x360/31d2000192851c1c56b2"
                }
            ],
            "width":788
        },
        {
            "height":435,
            "uri":"list/31c80003bb3a767b44f6",
            "url":"http://p3.pstatp.com/list/31c80003bb3a767b44f6",
            "url_list":[
                {
                    "url":"http://p3.pstatp.com/list/31c80003bb3a767b44f6"
                },
                {
                    "url":"http://pb9.pstatp.com/list/31c80003bb3a767b44f6"
                },
                {
                    "url":"http://pb1.pstatp.com/list/31c80003bb3a767b44f6"
                }
            ],
            "width":790
        },
        {
            "height":436,
            "uri":"list/31d400039527b0fcf128",
            "url":"http://p9.pstatp.com/list/31d400039527b0fcf128",
            "url_list":[
                {
                    "url":"http://p9.pstatp.com/list/31d400039527b0fcf128"
                },
                {
                    "url":"http://pb1.pstatp.com/list/31d400039527b0fcf128"
                },
                {
                    "url":"http://pb3.pstatp.com/list/31d400039527b0fcf128"
                }
            ],
            "width":781
        }
    ],
    "is_subject":false,
    "item_id":6448489556105758000,
    "item_version":0,
    "keywords":"Siri,苹果8,OLED,iPhone 8,A11",
    "level":0,
    "like_count":1,
    "log_pb":{
        "impr_id":"20170823200247010008035068933C4D"
    },
    "media_info":{
        "avatar_url":"http://p9.pstatp.com/large/3645001308888dbb1e43",
        "follow":false,
        "is_star_user":false,
        "media_id":1573055191383053,
        "name":"云端之战",
        "recommend_reason":"",
        "recommend_type":0,
        "user_id":63661084805,
        "user_verified":false,
        "verified_content":""
    },
    "media_name":"云端之战",
    "middle_image":{
        "height":438,
        "uri":"list/31d2000192851c1c56b2",
        "url":"http://p3.pstatp.com/list/300x196/31d2000192851c1c56b2.webp",
        "url_list":[
            {
                "url":"http://p3.pstatp.com/list/300x196/31d2000192851c1c56b2.webp"
            },
            {
                "url":"http://pb9.pstatp.com/list/300x196/31d2000192851c1c56b2.webp"
            },
            {
                "url":"http://pb1.pstatp.com/list/300x196/31d2000192851c1c56b2.webp"
            }
        ],
        "width":788
    },
    "preload_web":1,
    "publish_time":1501405974,
    "read_count":6704,
    "repin_count":13,
    "rid":"20170823200247010008035068933C4D",
    "share_count":0,
    "share_url":"http://toutiao.com/a6448485086420697357/?iid=13142832814&app=news_article",
    "show_portrait":false,
    "show_portrait_article":false,
    "source":"云端之战",
    "source_icon_style":4,
    "source_open_url":"sslocal://profile?uid=63661084805",
    "tag":"digital",
    "tag_id":6448485086420697000,
    "tip":0,
    "title":"网络流传iPhone 8 真机图片，就长这样了，还会买吗？",
    "ugc_recommend":{
        "activity":"",
        "reason":""
    },
    "url":"http://toutiao.com/group/6448485086420697357/",
    "user_info":{
        "avatar_url":"http://p3.pstatp.com/thumb/3645001308888dbb1e43",
        "description":"分享科技、武器资讯。",
        "follow":false,
        "follower_count":0,
        "name":"云端之战",
        "user_id":63661084805,
        "user_verified":false
    },
    "user_repin":0,
    "user_verified":0,
    "verified_content":"",
    "video_style":0
}
```

#### 3.一大图-视频

返回的数据：
```
{
    "log_pb":{
        "impr_id":"201708211321030100030262039088E6"
    },
    "read_count":131615,
    "video_id":"460cee0eb21340649f0736944fdfb463",
    "media_name":"u7206笑风云",
    "ban_comment":0,
    "abstract":"陈翔六点半：蘑菇头新提玛莎拉蒂2018款",
    "video_detail_info":{
        "group_flags":32832,
        "video_type":0,
        "video_preloading_flag":1,
        "video_url":[

        ],
        "direct_play":1,
        "detail_video_large_image":{
            "url":"http://p3.pstatp.com/video1609/35fe0015fb552c9f935f",
            "width":580,
            "url_list":[
                {
                    "url":"http://p3.pstatp.com/video1609/35fe0015fb552c9f935f"
                },
                {
                    "url":"http://pb9.pstatp.com/video1609/35fe0015fb552c9f935f"
                },
                {
                    "url":"http://pb1.pstatp.com/video1609/35fe0015fb552c9f935f"
                }
            ],
            "uri":"video1609/35fe0015fb552c9f935f",
            "height":326
        },
        "show_pgc_subscribe":1,
        "video_third_monitor_url":"",
        "video_id":"460cee0eb21340649f0736944fdfb463",
        "video_watching_count":0,
        "video_watch_count":205861
    },
    "image_list":[

    ],
    "ugc_recommend":{
        "reason":"",
        "activity":""
    },
    "article_type":0,
    "tag":"video_car",
    "forward_info":{
        "forward_count":0
    },
    "has_m3u8_video":0,
    "keywords":"蘑菇头,陈翔,玛莎拉蒂",
    "video_duration":273,
    "show_portrait_article":false,
    "user_verified":0,
    "aggr_type":1,
    "cell_type":0,
    "article_sub_type":0,
    "group_flags":32833,
    "bury_count":47,
    "title":"陈翔六点半：蘑菇头新提玛莎拉蒂2018款",
    "ignore_web_transform":1,
    "source_icon_style":1,
    "tip":0,
    "hot":0,
    "share_url":"http://toutiao.com/a6454936131342434829/?iid=13142832814&app=news_article",
    "has_mp4_video":0,
    "source":"爆笑风云",
    "comment_count":22,
    "article_url":"http://toutiao.com/group/6454936131342434829/",
    "filter_words":[
        {
            "id":"8:0",
            "name":"看过了",
            "is_selected":false
        },
        {
            "id":"9:1",
            "name":"内容太水",
            "is_selected":false
        },
        {
            "id":"5:623107913",
            "name":"拉黑作者:爆笑风云",
            "is_selected":false
        },
        {
            "id":"1:181604311",
            "name":"不想看:汽车视频",
            "is_selected":false
        },
        {
            "id":"6:139088",
            "name":"不想看:陈翔",
            "is_selected":false
        },
        {
            "id":"6:53463",
            "name":"不想看:玛莎拉蒂",
            "is_selected":false
        }
    ],
    "share_count":180,
    "rid":"201708211321030100030262039088E6",
    "video_play_info":{
        "status":10,
        "message":"success",
        "video_duration":273.87,
        "validate":"0",
        "enable_ssl":false,
        "poster_url":"http://p3.pstatp.com/origin/360300031f4e9cce8d55",
        "original_play_url":{
            "backup_url":"http://voffline.pstatp.com/audit/m/f19800002310d83b9f36/",
            "main_url":"http://voffline.pstatp.com/audit/m/f19800002310d83b9f36/"
        },
        "video_list":{
            "video_1":{
                "definition":"360p",
                "vtype":"mp4",
                "vwidth":640,
                "vheight":360,
                "bitrate":426506,
                "logo_name":"xigua",
                "coded_format":"h264",
                "size":16922425,
                "main_url":"aHR0cDovL3YxLXR0Lml4aWd1YS5jb20vMjlkNDM5MWQ5ZTMwODgyMTc0NDZlNmEwMWM4YmVlODYvNTk5YTZkYzAvdmlkZW8vbS8yMjA0ZmRlNDc3NGNlMGE0MjUwODY2YTQ4OTM1ZmYyYThhZDExNGYyZjQwMDAwNmU1ODRiMzgwNGRiLw==",
                "backup_url_1":"aHR0cDovL3Y3LnBzdGF0cC5jb20vYmI1NzE2MzczNmM4ZDI5Mjg4ZjkzYTg4M2E5OGJlZWUvNTk5YTZkYzAvdmlkZW8vbS8yMjA0ZmRlNDc3NGNlMGE0MjUwODY2YTQ4OTM1ZmYyYThhZDExNGYyZjQwMDAwNmU1ODRiMzgwNGRiLw==",
                "user_video_proxy":1,
                "socket_buffer":255903600,
                "preload_size":327680,
                "preload_interval":25,
                "preload_min_step":5,
                "preload_max_step":10
            }
        },
        "dns_info":{

        }
    },
    "publish_time":1502906934,
    "action_list":[
        {
            "action":1,
            "extra":{

            },
            "desc":""
        },
        {
            "action":3,
            "extra":{

            },
            "desc":""
        },
        {
            "action":7,
            "extra":{

            },
            "desc":""
        },
        {
            "action":9,
            "extra":{

            },
            "desc":""
        }
    ],
    "cell_layout_style":1,
    "tag_id":6454936131342435000,
    "video_style":2,
    "verified_content":"",
    "display_url":"http://toutiao.com/group/6454936131342434829/",
    "large_image_list":[
        {
            "url":"http://p3.pstatp.com/video1609/35fe0015fb552c9f935f",
            "width":580,
            "url_list":[
                {
                    "url":"http://p3.pstatp.com/video1609/35fe0015fb552c9f935f"
                },
                {
                    "url":"http://pb9.pstatp.com/video1609/35fe0015fb552c9f935f"
                },
                {
                    "url":"http://pb1.pstatp.com/video1609/35fe0015fb552c9f935f"
                }
            ],
            "uri":"video1609/35fe0015fb552c9f935f",
            "height":326
        }
    ],
    "media_info":{
        "user_id":54622538049,
        "verified_content":"",
        "avatar_url":"http://p3.pstatp.com/large/13540016473c776259a0",
        "media_id":1556951777514498,
        "name":"爆笑风云",
        "recommend_type":0,
        "follow":false,
        "recommend_reason":"",
        "is_star_user":false,
        "user_verified":false
    },
    "item_id":6454936131342435000,
    "is_subject":false,
    "show_portrait":false,
    "repin_count":511,
    "cell_flag":75,
    "user_info":{
        "verified_content":"",
        "avatar_url":"http://p3.pstatp.com/thumb/13540016473c776259a0",
        "user_id":54622538049,
        "name":"爆笑风云",
        "follower_count":0,
        "follow":false,
        "user_auth_info":"",
        "user_verified":false,
        "description":"我负责搞笑，你们负责笑"
    },
    "source_open_url":"sslocal://profile?refer=video&uid=54622538049",
    "level":0,
    "like_count":269,
    "digg_count":269,
    "behot_time":1503291345,
    "cursor":1503291345999,
    "url":"http://toutiao.com/group/6454936131342434829/",
    "preload_web":0,
    "user_repin":0,
    "has_image":false,
    "item_version":0,
    "has_video":true,
    "group_id":6454936131342435000,
    "middle_image":{
        "url":"http://p3.pstatp.com/list/300x196/35fe0015fb552c9f935f.webp",
        "width":640,
        "url_list":[
            {
                "url":"http://p3.pstatp.com/list/300x196/35fe0015fb552c9f935f.webp"
            },
            {
                "url":"http://pb9.pstatp.com/list/300x196/35fe0015fb552c9f935f.webp"
            },
            {
                "url":"http://pb1.pstatp.com/list/300x196/35fe0015fb552c9f935f.webp"
            }
        ],
        "uri":"list/35fe0015fb552c9f935f",
        "height":360
    }
}
```

#### 4.一小图

返回的数据：
```
{
    "log_pb":{
        "impr_id":"20170823193708010008078081324061"
    },
    "read_count":17651,
    "media_name":"军路",
    "ban_comment":0,
    "abstract":"",
    "image_list":[

    ],
    "ugc_recommend":{
        "reason":"头条号原创作者",
        "activity":""
    },
    "article_type":0,
    "tag":"emotion",
    "forward_info":{
        "forward_count":0
    },
    "has_m3u8_video":0,
    "rid":"20170823193708010008078081324061",
    "show_portrait_article":false,
    "user_verified":1,
    "aggr_type":1,
    "cell_type":0,
    "article_sub_type":0,
    "bury_count":0,
    "title":"女朋友要这么撩，都学着点",
    "ignore_web_transform":1,
    "source_icon_style":5,
    "tip":0,
    "hot":0,
    "share_url":"http://toutiao.com/a6457262317569573390/?iid=13142832814&app=news_article",
    "has_mp4_video":0,
    "source":"军路",
    "comment_count":10,
    "article_url":"http://toutiao.com/group/6457262317569573390/",
    "filter_words":[
        {
            "id":"8:0",
            "name":"看过了",
            "is_selected":false
        },
        {
            "id":"9:1",
            "name":"内容太水",
            "is_selected":false
        },
        {
            "id":"5:61981476",
            "name":"拉黑作者:军路",
            "is_selected":false
        },
        {
            "id":"1:1650",
            "name":"不想看:两性",
            "is_selected":false
        }
    ],
    "share_count":17,
    "publish_time":1503448542,
    "action_list":[
        {
            "action":1,
            "extra":{

            },
            "desc":""
        },
        {
            "action":3,
            "extra":{

            },
            "desc":""
        },
        {
            "action":7,
            "extra":{

            },
            "desc":""
        },
        {
            "action":9,
            "extra":{

            },
            "desc":""
        }
    ],
    "gallary_image_count":4,
    "cell_layout_style":1,
    "tag_id":6457262317569574000,
    "video_style":0,
    "verified_content":"头条号原创作者",
    "display_url":"http://toutiao.com/group/6457262317569573390/",
    "large_image_list":[

    ],
    "media_info":{
        "user_id":5503109311,
        "verified_content":"",
        "avatar_url":"http://p3.pstatp.com/large/4110003be258e2c49d6",
        "media_id":5502535968,
        "name":"军路",
        "recommend_type":0,
        "follow":false,
        "recommend_reason":"",
        "is_star_user":false,
        "user_verified":true
    },
    "item_id":6457262317569574000,
    "is_subject":false,
    "show_portrait":false,
    "repin_count":239,
    "cell_flag":11,
    "user_info":{
        "verified_content":"头条号原创作者",
        "avatar_url":"http://p1.pstatp.com/thumb/4110003be258e2c49d6",
        "user_id":5503109311,
        "name":"军路",
        "follower_count":0,
        "follow":false,
        "user_auth_info":{
            "auth_type":"0",
            "other_auth":{
                "pgc":"头条号原创作者"
            },
            "auth_info":"头条号原创作者"
        },
        "user_verified":true,
        "description":"凝聚万千军人军属，还原一个真实军营。"
    },
    "source_open_url":"sslocal://profile?uid=5503109311",
    "level":0,
    "like_count":1,
    "digg_count":1,
    "behot_time":1503488225,
    "cursor":1503488225999,
    "url":"http://toutiao.com/group/6457262317569573390/",
    "preload_web":1,
    "user_repin":0,
    "has_image":true,
    "item_version":0,
    "has_video":false,
    "group_id":6457262317569574000,
    "middle_image":{
        "url":"http://p9.pstatp.com/list/300x196/3643000c735249235dc4.webp",
        "width":907,
        "url_list":[
            {
                "url":"http://p9.pstatp.com/list/300x196/3643000c735249235dc4.webp"
            },
            {
                "url":"http://pb1.pstatp.com/list/300x196/3643000c735249235dc4.webp"
            },
            {
                "url":"http://pb3.pstatp.com/list/300x196/3643000c735249235dc4.webp"
            }
        ],
        "uri":"list/3643000c735249235dc4",
        "height":510
    }
}
```
