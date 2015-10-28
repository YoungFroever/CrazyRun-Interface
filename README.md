# 暴走日报接口
以下所有 API 均由 __暴走日报（http://baozouribao.com/）__ 提供，本人（YoungFroever）采取非正常手段获取。获取与共享之行为或有侵犯暴走日报权益的嫌疑。若被告知需停止共享与使用，本人会及时删除此页面与整个项目。  
请您暸解相关情况，并遵守暴走日报协议。
# API说明
* 知乎日报的消息以 JSON 格式输出
* 以下所有 API 使用的 HTTP Method 均为 `GET`
* 
* ### 1. 启动界面图像获取
* URL: `http://daily.ibaozou.com/api/2/start-image/720*1280`  
* `start-image` 后为图像分辨率

* 响应实例：

 {
  "text": "",
  "img": "http://ww3.sinaimg.cn/mw690/da4a9471jw1eplohwd8gbj20k00zk7ae.jpg"
}

* 分析：
    * `text` : 供显示的图片版权信息
    * `img` : 图像的 URL

