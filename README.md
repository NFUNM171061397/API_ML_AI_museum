# 智能博物馆
| 发布时间 | 2019-12-05 |
| ------  | -------:   |
| 文档名称 |  智能博物馆  |
| 文档状态 |  已完成     |
| 产品设计师  |  张柳燕    |
|  产品开发者 |  张柳燕    |
| 产品测试员|  张柳燕    |

## 价值主张设计（一句话版本）
智能博物馆APP为用户提供了展品搜索与路线推荐这两大功能，能够为用户推荐前往相关展区的最佳浏览路线，以及提供全程的语音导览，为用户用文字及语音方式介绍相关展品，是一款能够帮助用户提升观展体验的软件。

## 价值主张设计（一分钟版本）
### 加值宣言
智能毕业纪念册APP拥有展品搜索与路线推荐这两大核心功能，通过调用路径规划API、普通IP定位功能、图像识别API、语音识别API和语音合成API，为用户提供最佳观展路线以及展品的导览。能够帮助用户快速到达目标展区、实时为用户更新自己在博物馆的所处位置、帮助用户更好的了解展品资料。解决了用户在进入博物馆之后，不知道按照什么路线观展，不知道自己的所处位置，想了解更多展品有关信息身边却没有导游等问题，是一款可以帮助用户提高观展体验的软件。

### 核心价值（最小可行性产品）
###### 功能一：定位地理信息（区域地理信息）
用户能够获得在展馆内精准的定位信息，知道自己所处位置；提供导航功能，用户输入相关展区/展品，就能为用户规划最佳观展路线。

###### 功能二：图像识别与语音识别
用户可以对展品上的二维码进行扫描，APP能够返回相对应展品的详细资料；将用户传入的语音识别成文本输出，对展品进行搜索，返回相对应展品的详细资料。

###### 功能三：文本内容转化为语音内容
用户在参观展品时，可以选择把APP上展品的详细资料，将文字内容转化为语音输出，给予用户介绍展品的功能。

### 核心价值与用户痛点
* 用户想要随时查看展馆的地图分布，知道自己所在的地点，而不用到处找指示地图。
* 用户人员有想要前往的展品区，希望能快速到达目的地。
* 用户想了解展品信息，但是身边却没有导游。
* 用户想快速到达目标展区，但在小区域内使用常用的导航app效果甚微。


### 人工智能概率性与用户痛点
- 用户上传/拍摄的照片清晰度过低，无法进行识别
- 用户所在位置信号差，无法实时更新用户在博物馆的所处位置
- 用户上传的语音太模糊，所处环境太嘈杂，无法进行识别

### 需求列表与人工智能API加值
| 用户案例 | 人工智能api | 重要程度 |
| ------  | -------:   | -------   |
| 用户想要快速到达目标展区 |  路径规划 | 重要
| 用户想要知道自己当前所处位置 |  普通IP定位功能 | 重要 |
| 用户想要了解当前展品信息 |  图像识别-扫描二维码 | 重要 |
| 用户想要了解当前展品信息 |  语音识别-语音搜索展品 |重要 |
| 用户想要使用语音导览 |  语音合成-语音解说  |重要 |


## 产品原型
* 产品功能模块
![产品原型](https://gitee.com/NFUNM171061397/API_ML_AI/raw/master/image/WechatIMG896.jpeg)
* 个人中心模块
![个人中心](https://gitee.com/NFUNM171061397/API_ML_AI/raw/master/image/WechatIMG895.jpeg)

### 1.交互及界面设计（详见上文图片/原型）
* 路线模块：路径规划API、普通IP定位API
* 资料模块：图像识别API、语音识别API、语音合成API

### 2.信息设计（详见上文图片/原型）
* 返回的展品详细资料：图像识别API、语音识别API
* 语音导览：展品资料、语音合成API

### 3.[产品原型](http://nfunm171061397.gitee.io/api_ml_ai_museum)

### 4.口头操作说明（详见上文图片/原型）
* 路径模块：用户点击上方按钮，通过普通IP定位功能，返回用户在展馆内所处位置。用户点击下方按钮，跳转路径规划功能页面，用户可以输入目标展区/语音输入，系统将返回最佳路径规划。
* 信息模块：主页可以通过三种方式将信息输入：打字输入/拍照输入/语音输入。用户打字输入，直接返回结果；用户点击拍照按钮，页面跳转至二维码扫描页面，用户传入照片，系统通过调用图像识别API进行识别，返回展品信息；用户点击语音按钮，页面跳转至语音识别页面，用户传入语音，系统通过调用语音识别API进行识别，返回展品信息。
* 个人中心：用户可依照个人所需使用功能。

