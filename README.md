# 暴走日报接口
以下所有 API 均由 __暴走日报（http://baozouribao.com/）__ 提供，本人（YoungFroever）采取非正常手段获取。获取与共享之行为或有侵犯暴走日报权益的嫌疑。若被告知需停止共享与使用，本人会及时删除此页面与整个项目。  
请您暸解相关情况，并遵守暴走日报协议。

# API说明
* 知乎日报的消息以 JSON 格式输出
* 以下所有 API 使用的 HTTP Method 均为 `GET`

# API分析
 ### 1. 启动界面图像获取
* URL: `http://daily.ibaozou.com/api/2/start-image/720*1280`  

* 响应实例：

  {
            text: "",
            img: "http://ww3.sinaimg.cn/mw690/da4a9471jw1eplohwd8gbj20k00zk7ae.jpg"
        }  

* 分析：
    * `img` : 图像的 URL

 ### 2.最新
 * URL:`http://ribao.ibaozou.com/api/v1/articles/latest`
 * 响应实例:
                  {
            articles: [
                {
            "title": "大导演的怪癖——鬼才徐克的百合情色~",
            "image": "http://ww4.sinaimg.cn/large/005YbKTXjw1exh3npqhpsj30hs0hstbe.jpg",
            "video_file_url": "",
            "thumbnail": "http://ww1.sinaimg.cn/large/005ZSZBTjw1exh3nq9yc6j303c03ca9x.jpg",
            "author_avatar": "http://ww4.sinaimg.cn/large/e8fffd59jw1ewj4gsa5mwj20dw0dwdgy.jpg",
            "author_name": "大脸侠",
            "share_image": "http://7o51ui.com1.z0.glb.clouddn.com/e3bd2e005f9001332ddf5254005a9dab.jpg",
            "key_words": "大脸侠 大导演的怪癖——鬼才徐克的百合情色   电影收割机",
            "id": "6883519",
            "video_image_url": "",
            "section_id": 124,
            "display_date": "10 月 28 日",
            "ga_prefix": "102820",
            "vote_count": 42,
            "share_url": "http://baozouribao.com/articles/6883519",
            "url": "http://dailyapi.ibaozou.com/api/v1/articles/6883519",
            "tag": "",
            "guide": "",
            "guide_image": "",
            "hit_count": 46740,
            "section_name": "电影收割机",
            "section_image": "http://ww4.sinaimg.cn/small/0062RSUgjw1ewkh4h5u3xj30f00a0glx.jpg",
            "hit_count_string": "4.67万",
            "author_summary": "我的女朋友比男编辑的都多。 "
            ],
           ...
            "date": "20151028",
            "display_date": "2015.10.28 星期三",
            "is_today": true
             }
* 重点分析：
    * `articles` : 当日新闻
        * `image` : 大图
        * `thumbnail` : 小图
        * `video_file_url` : 视频播放地址，点击即可播放
        * `tag` : cell中显示的小的图片，可为空，或者为视频，热点等
        * `id` : 拼接详情页的http: http://ribao.ibaozou.com/api/v3/article/id
    * `date` : 今日，其中在每日接口中返回上一页的数据，如今天是20151028，date显示20151027，可方便下拉加载
* 由于接口类似，不明白的可以点击去看，所以往后就不再一一说了

### 3.每日
* URL:`http://ribao.ibaozou.com/api/v1/articles/before/20151028`

### 4.最新
* URL:`http://ribao.ibaozou.com/api/v1/articles/latest`

### 4.最热
* URL:`http://daily.ibaozou.com/api/2/articles/hot`
* 
### 5.详情
* URL:`http://ribao.ibaozou.com/api/v3/article/(点击传进来的id)`

### 6.评论
* URL:`http://dailyapi.ibaozou.com/api/v1/articles/（点击传进来的id）/n_comments?page=1`

### 6.投票及投票数
* URL:`http://daily.ibaozou.com/api/2/article-extra/（点击传进来的id）`

### 6.各个板块
* URL:`http://daily.ibaozou.com/api/2/section/(数字，下面有说明)`
* 打开接口可以看到最后提供了一个时间戳，可以根据时间戳来加载以前的内容
* 以前的内容URL:`http://daily.ibaozou.com/api/2/section/数字/before/时间戳`
* 32：初安遇上电影
* 41：啊Mui的漫画
* 42：韩国深井冰漫画 - 楚力
* 44. P神联盟
* 47. 战乱夕阳教你…
* 49. 直击暴走大事件
* 53. 每日一暴	
* 54. 编辑部的故事
* 55. 恶搞四格
* 56. 小鸡育儿记
* 57. 暴走动漫资讯
* 58  暴走娱乐资讯
* 60. 暴走小课堂
* 61. 再穷也要去旅行
* 62. 暴走看啥片
* 64. 暴走恐怖故事
* 65. 读·文
* 81. 大爷来玩儿❤
* 83. 暴走科技资讯
* 85. 看魔术涨姿势
* 86. Yuki的时尚课堂
* 90. 诡异事件簙
* 91. 阿宅漫研社
* 94. 强中自有强中手
* 95. 面粉一家亲
* 96. 奇闻录
* 100. 小海狮温比历险记
* 101. 不明飞行物体
* 102. 图文大事件
* 103. APP爱啪啪
* 104. 动物园真相
* 119. 学霸追剧攻略
* 120. 游戏拯救智障
* 123. 长袖遇上电影
* 124. 电影收割机
* 125. 贵圈真乱

这是我第一次在github上写东西，格式参考了`https://github.com/izzyleung/ZhihuDailyPurify/wiki/%E7%9F%A5%E4%B9%8E%E6%97%A5%E6%8A%A5-API-%E5%88%86%E6%9E%90`的格式布局，在此深表感谢。本人是iOS初学者，目前正在寻找第一份工作，由于众所周知的原因许多公司都不愿意要没有经验的非重点大学的毕业生，再加上本人不善表达找工作的路程不太顺利。如果您能看到这并且您的公司有适合我的初级iOS开发职位请帮我内推一下，在此深表感激！
* PS:如果真有人看到这的话留一下邮箱:yangjianchengan@163.com
* 如果有一天我真的成大牛了看到以前的自己也会感慨一下吧。YJ留于2015.10.28
