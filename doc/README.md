# 酷我音乐Api



## 接口文档

#### 播放链接

接口: `/url=80958029`

| 参数  | 说明    | 是否必须 | 示例            |
| ----- | ------- | -------- | --------------- |
| `sid` | 歌曲 id | 是       | `sid` =80958029 |



#### 歌词

示例: `/lrc?musicId=80958029`

| 参数      | 说明   | 是否必须 | 示例               |
| --------- | ------ | -------- | ------------------ |
| `musicId` | 音乐id | 是       | `musicId`=80958029 |
|           |        |          |                    |



#### 搜索

接口: `/search/searchMusicBykeyWord?key=我要找到你` 

参数 : `searchKey` 熱搜詞   `searchMusicBykeyWord` 單曲`searchAlbumBykeyWord` 專輯`searchMvBykeyWord` mv `searchPlayListBykeyWord` 歌单  `searchArtistBykeyWord` 歌手

| 参数  | 说明       | 是否必须   | 示例             |
| ----- | ---------- | ---------- | ---------------- |
| `key` | 搜索关键字 | 是         | key = 我要找到你 |
| `pn`  | 页数       | 否 默认 1  | `pn `= 2         |
| `rn`  | 每页数量   | 否 默认 30 | `rn `=  15       |



#### 轮播图

接口: `/banner`  

```json
{
"code": 200,
"curTime": 1581397195179,
"data": [
{
"id": 1,
"pic": "http://kwimg4.kuwo.cn/star/upload/47/52/1557311466098_.png",
"priority": 1,
"url": "http://down.kuwo.cn/mbox/kwmusic_web_1.exe"
},
{
"id": 18,
"pic": "http://kwimg2.kuwo.cn/star/upload/12/15/1581389006583_.jpg",
"priority": 2,
"url": "http://www.kuwo.cn/album_detail/12554981"
},
{
"id": 10,
"pic": "http://kwimg4.kuwo.cn/star/upload/76/42/1581305352340_.jpg",
"priority": 3,
"url": "http://www.kuwo.cn/album_detail/12720213"
},
{
"id": 9,
"pic": "http://kwimg3.kuwo.cn/star/upload/72/82/1581305211162_.jpg",
"priority": 4,
"url": "http://www.kuwo.cn/album_detail/7662111"
},
{
"id": 11,
"pic": "http://kwimg2.kuwo.cn/star/upload/2/94/1581092599880_.jpg",
"priority": 5,
"url": "http://www.kuwo.cn/playlist_detail/2952464073"
},
{
"id": 19,
"pic": "http://kwimg4.kuwo.cn/star/upload/1/51/1581220186723_.jpg",
"priority": 6,
"url": "http://www.kuwo.cn/playlist_detail/2950090991"
},
{
"id": 20,
"pic": "http://kwimg3.kuwo.cn/star/upload/34/71/1580525755117_.jpg",
"priority": 7,
"url": "http://www.kuwo.cn/playlist_detail/2948964151"
},
{
"id": 7,
"pic": "http://kwimg1.kuwo.cn/star/upload/6/66/1579069807332_.jpg",
"priority": 8,
"url": "http://jx.kuwo.cn/KuwoLive/OpenLiveRoomLinkForKw?from=1001004053"
}
],
"msg": "success",
"profileId": "site",
"reqId": "be53e268b062aa76eca763beb8a7f071"
}
```



#### 评论

接口: `/comment？sid=80958029&type=get_rec_comment&page=1&rows=30&digest=15`

| 参数     | 说明                                                | 是否必须 | 示例                   |
| -------- | --------------------------------------------------- | -------- | ---------------------- |
| `sid`    | 评论类型 id                                         | 是       | `sid`=80958029         |
| `page`   | 页数                                                |          |                        |
| `rows`   | 每页条数                                            |          | 默认 30                |
| `type`   | `get_rec_comment`  热门评论  `get_comment` 最新评论 |          | 默认 `get_rec_comment` |
| `digest` | 15 歌曲  2 排行榜  7 mv评论  8 歌单评论             |          | 默认 `15`              |

#### mv播放地址

接口: `/mv_url?rid=4301188`

| 参数 | 说明  | 是否必须 | 示例        |
| ---- | ----- | -------- | ----------- |
| rid  | mv id | 是       | rid=4301188 |

### 歌单

#### - 推薦歌單

接口:`/rec_gedan` 

| 參數 | 説明     | 是否必須 | 示例  |
| ---- | -------- | -------- | ----- |
| rn   | 分頁     |          | 默認1 |
| pn   | 每頁數量 |          | 默認5 |



#### - 默认歌单

接口: `/playList`

示例:`/playList?order=new&rn=30&pn=1` 

| 参数  | 说明               | 是否必须 | 示例     |
| ----- | ------------------ | -------- | -------- |
| order | new 最新  hot 最热 |          | 默认 new |
| rn    | 每页条数           |          | 默认 30  |
| pn    | 页数               |          | 默认 1   |

#### - 歌单分类

示例：`/playList/category?id=2190`

| 参数 | 说明        | 是否必须 | 示例      |
| ---- | ----------- | -------- | --------- |
| id   | 歌单 tag id | 是       | id = 2190 |
| rn   | 每页条数    |          | 默认 30   |
| pn   | 页数        |          | 默认1     |



#### - 歌单分类Tag

接口:`/playList_tags`

```json
{
"img": "http://img2.kwcdn.kuwo.cn/star/upload/11/11/1531190823851_.png",
"mdigest": "5",
"data": [
{
"extend": "",
"img": "http://img2.kwcdn.kuwo.cn/star/upload/15/15/1536566688335_.jpg",
"digest": "10000",
"name": "翻唱",
"isnew": "0",
"id": "1848"
},
{
"extend": "",
"img": "http://img4.kwcdn.kuwo.cn/star/upload/13/13/1507883183437_.png",
"digest": "10000",
"name": "网络",
"isnew": "0",
"id": "621"
},
{
"extend": "",
"img": "http://img1.kwcdn.kuwo.cn/star/upload/6/6/1507883159190_.png",
"digest": "10000",
"name": "经典",
"isnew": "0",
"id": "1265"
},
{
"extend": "",
"img": "http://img1.kwcdn.kuwo.cn/star/upload/0/0/1507781397648_.png",
"digest": "10000",
"name": "轻音乐",
"isnew": "0",
"id": "173"
},
{
"extend": "",
"img": "http://img3.kwcdn.kuwo.cn/star/upload/7/7/1517380561751_.png",
"digest": "10000",
"name": "怀旧",
"isnew": "0",
"id": "155"
},
{
"extend": "",
"img": "http://img4.kwcdn.kuwo.cn/star/upload/11/11/1517380562443_.png",
"digest": "10000",
"name": "古风",
"isnew": "0",
"id": "127"
},
{
"extend": "",
"img": "http://img3.kwcdn.kuwo.cn/star/upload/7/7/1517380562103_.png",
"digest": "10000",
"name": "网红",
"isnew": "0",
"id": "1879"
},
{
"extend": "",
"img": "http://img3.kwcdn.kuwo.cn/star/upload/8/8/1507781342248_.png",
"digest": "10000",
"name": "佛乐",
"isnew": "0",
"id": "220"
},
{
"extend": "",
"img": "http://img3.kwcdn.kuwo.cn/star/upload/7/7/1517380562103_.png",
"digest": "10000",
"name": "影视",
"isnew": "0",
"id": "180"
},
{
"extend": "",
"img": "http://img4.kwcdn.kuwo.cn/star/upload/15/15/1507883255871_.png",
"digest": "10000",
"name": "器乐",
"isnew": "0",
"id": "578"
},
{
"extend": "",
"img": "http://img3.kwcdn.kuwo.cn/star/upload/9/9/1517380562105_.png",
"digest": "10000",
"name": "游戏",
"isnew": "0",
"id": "1877"
},
{
"extend": "",
"img": "http://img1.kwcdn.kuwo.cn/star/upload/10/10/1517468038218_.png",
"digest": "10000",
"name": "国漫游戏",
"isnew": "0",
"id": "181"
},
{
"extend": "",
"img": "http://img3.kwcdn.kuwo.cn/star/upload/10/10/1507883200970_.png",
"digest": "10000",
"name": "KTV",
"isnew": "0",
"id": "361"
},
{
"extend": "",
"img": "http://img1.kwcdn.kuwo.cn/star/upload/5/5/1517380561685_.png",
"digest": "10000",
"name": "喊麦",
"isnew": "0",
"id": "216"
},
{
"extend": "|HOT",
"img": "http://img4.kwcdn.kuwo.cn/star/upload/3/3/1536566652003_.jpg",
"digest": "10000",
"name": "抖音",
"isnew": "0",
"id": "2189"
},
{
"extend": "",
"img": "http://kwimg4.kuwo.cn/star/upload/16/73/1551434397397_.jpg",
"digest": "10000",
"name": "3D",
"isnew": "0",
"id": "1366"
},
{
"extend": "",
"img": "http://img2.kwcdn.kuwo.cn/star/upload/15/15/1517380562303_.png",
"digest": "10000",
"name": "店铺专用",
"isnew": "0",
"id": "263"
},
{
"extend": "",
"img": "http://img3.kwcdn.kuwo.cn/star/upload/14/14/1524130384286_.png",
"digest": "10000",
"name": "纯音乐",
"isnew": "0",
"id": "577"
},
{
"extend": "|NEW",
"img": "http://kwimg2.kuwo.cn/star/upload/40/75/1579227646729_.jpg",
"digest": "10000",
"name": "春节",
"isnew": "0",
"id": "2190"
}
],
"name": "主题",
"id": "5",
"type": "list",
"img1": "http://kwimg2.kuwo.cn/star/upload/46/19/1548987670837_.png"
},
```





### 歌手 

#### - 全部歌手

接口：

+ `/singer?category=0&rn=100&pn=1`
+ `/singer?category=0&rn=100&pn=1&prefix=A`

參數: 分类： 0 = 全部 1 = 华语男 2 = 华语女 3 = 华语组合 4 = 日韩男 5 = 日韩女 6 = 日韩组合 7 = 欧美男 8 = 欧美女 9 = 欧美组合 10 = 其他

| 參數     | 説明     | 是否必須 | 示例    |
| -------- | -------- | -------- | ------- |
| category | 分類     | 是       | 默認 0  |
| rn       | 每頁數量 |          | 默認100 |
| pn       | 分頁     |          | 默認1   |
| prefix   | A~Z 分類 |          |         |

#### - 歌手單曲

接口:`/singer/music?artistid=5371&rn=30&pn=1`

| 參數     | 説明     | 是否必須 | 示例          |
| -------- | -------- | -------- | ------------- |
| artistid | 歌手id   | 是       | artistid=5371 |
| rn       | 每頁數量 |          | 默認30        |
| pn       | 分頁     |          | 默認1         |

#### - 歌手專輯

接口:`/singer/album?artistid=5371&rn=30&pn=1`

| 參數     | 説明     | 是否必須 | 示例          |
| -------- | -------- | -------- | ------------- |
| artistid | 歌手id   | 是       | artistid=5371 |
| rn       | 每頁數量 |          | 默認30        |
| pn       | 分頁     |          | 默認1歌手mv   |

#### - 歌手mv

| 參數     | 説明     | 是否必須 | 示例          |
| -------- | -------- | -------- | ------------- |
| artistid | 歌手id   | 是       | artistid=5371 |
| rn       | 每頁數量 |          | 默認30        |
| pn       | 分頁     |          | 默認1         |

#### - 歌手推薦

接口: `/rec_singer`

示例: `/rec_singer?category=11&rn=6&pn=1`

| 參數     | 説明     | 是否必須 | 示例   |
| -------- | -------- | -------- | ------ |
| category | 分類     |          | 默認11 |
| rn       | 每頁數量 |          | 默認6  |
| pn       | 頁數     |          | 默認1  |



### 音樂信息

接口:`/musicInfo?mid=6691107`

| 參數 | 説明   | 是否必須 | 示例        |
| ---- | ------ | -------- | ----------- |
| mid  | 音樂id | 是       | mid=6691107 |



### 排行榜

#### - 排行榜單

接口：`/rank`

```json
{
"name": "官方榜",
"list": [
{
"sourceid": "93",
"intro": "酷我用户每天播放线上歌曲的飙升指数TOP排行榜，为你展示流行趋势、蹿红歌曲，每天更新",
"name": "酷我飙升榜",
"id": "489929",
"source": "2",
"pic": "http://img3.kwcdn.kuwo.cn/star/upload/4/9/1581375962.png",
"pub": "今日更新"
},
{
"sourceid": "17",
"intro": "酷我用户每天播放新歌（一个月内发行）TOP排行榜，为你展示当下潮流新歌，每天更新",
"name": "酷我新歌榜",
"id": "489928",
"source": "2",
"pic": "http://img3.kwcdn.kuwo.cn/star/upload/6/9/1581203155.png",
"pub": "今日更新"
},
{
"sourceid": "16",
"intro": "酷我用户每天播放线上歌曲TOP排行榜，为你展示当下最人气最热门歌曲，每天更新",
"name": "酷我热歌榜",
"id": "489927",
"source": "2",
"pic": "http://img3.kwcdn.kuwo.cn/star/upload/2/4/1581030357.png",
"pub": "今日更新"
},
{
"sourceid": "158",
"intro": "抖音官方热歌TOP排行榜，为你展示最火最洗脑的抖音神曲，每周二更新",
"name": "抖音热歌榜",
"id": "490022",
"source": "2",
"pic": "http://img3.kwcdn.kuwo.cn/star/upload/4/2/1581375964.png",
"pub": "今日更新"
},
{
"sourceid": "145",
"intro": "酷我音乐包歌曲TOP排行榜，为你展示最卖座的高品质无损音乐，每天更新",
"name": "会员畅听榜",
"id": "507077",
"source": "2",
"pic": "http://img3.kwcdn.kuwo.cn/star/upload/1/6/1580598361.png",
"pub": "今日更新"
}
]
}
```

#### - 排行榜音樂

接口:`/rank/musicList`

示例:	`/rank/musicList?bangId=93&pn=1&rn=30`

| 參數   | 説明     | 是否必須 | 示例      |
| ------ | -------- | -------- | --------- |
| bangId | 榜單id   | 是       | bangId=93 |
| pn     | 分頁     |          | 默認1     |
| rn     | 每頁數量 |          | 默認30    |

#### - 推薦榜單

接口:`/rank/rec_bangList` 

```json
{
"leader": "酷我热歌榜",
"num": "350",
"name": "酷我热歌榜",
"pic": "http://img1.kwcdn.kuwo.cn/star/upload/12/12/1481783559612_.png",
"id": "16",
"pub": "2020-02-11",
"musicList": [8 items]
}
```



### 主播電臺

接口:`/radio`

```json
Tree
Chart
JSON Input
{
"code": 200,
"curTime": 1581407319418,
"data": {
"albumList": [
{
"artist": "蕊希Erin",
"album": "蕊希电台",
"listencnt": "30933",
"pic": "http://img3.kuwo.cn/star/albumcover/300/52/43/2233596567.jpg",
"rid": "38721812"
},
{
"artist": "由小藜",
"album": "非藜不可",
"listencnt": "145635",
"pic": "http://img3.kuwo.cn/star/albumcover/300/40/46/3747600081.jpg",
"rid": "51859818"
},
{
"artist": "睡前一起夜听",
"album": "睡前一起夜听 ",
"listencnt": "5537",
"pic": "http://img3.kuwo.cn/star/albumcover/500/8/74/538223138.jpg",
"rid": "63807800"
},
{
"artist": "紫云纱",
"album": "职场情报局",
"listencnt": "154056",
"pic": "http://img3.kuwo.cn/star/albumcover/300/56/78/4005148811.jpg",
"rid": "39277769"
},
{
"artist": "北城[主播]",
"album": "南城故事",
"listencnt": "210292",
"pic": "http://img4.kuwo.cn/star/albumcover/300/47/92/186765640.jpg",
"rid": "40887125"
},
{
"artist": "中国大百科全书出版社",
"album": "迷你百科脱口秀第二季",
"listencnt": "1741",
"pic": "http://img4.kuwo.cn/star/albumcover/300/79/11/1935561670.jpg",
"rid": "63722836"
},
{
"artist": "喜剧听我的",
"album": "小沈阳爆笑作品汇",
"listencnt": "69499",
"pic": "http://img3.kuwo.cn/star/albumcover/300/6/0/1039562571.jpg",
"rid": "68390546"
},
{
"artist": "凯紫",
"album": "诗词之美",
"listencnt": "27520",
"pic": "http://img4.kuwo.cn/star/albumcover/300/2/94/1939976936.jpg",
"rid": "61002763"
},
{
"artist": "九小如",
"album": "【美文】听说-你的心情有人懂",
"listencnt": "376042",
"pic": "http://img1.kuwo.cn/star/albumcover/300/29/84/1778172532.jpg",
"rid": "41327034"
}
]
},
"msg": "success",
"profileId": "site",
"reqId": "cd681719285c24cb5db83494e7fbf0eb"
}
```
