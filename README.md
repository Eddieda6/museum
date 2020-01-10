#### 介绍
本仓库存放博物馆产品文档： **为博物馆动静结合智能管理**  

#### "博物馆"产品文档版本

| 产品状态         | 未完成          |
| ---------------- | --------------- |
| 产品负责人       | 唐颖欣          |
| 产品文档编辑     | 唐颖欣          |
| 最后修改时间     | 1.5 / 16：21 |
| 产品预计上线时间 | 2019.12.30      |

### “博物馆”产品文档概述  

|PRD价值主张设计|原型设计|
| --- | --- |
|<a href="#1">加值宣言</a>|<a href="#21">交互及界面设计</a>|
|<a href="#2">核心价值</a>|<a href="#22">信息设计</a>|
|<a href="#3">用户痛点</a>|<a href="#23">原型文档</a>|
|<a href="#4">人工智能概率性</a>|<a href="#24">口头操作说明</a>|
|<a href="#5">需求列表</a>|



### PRD价值主张设计

#### <a name="1">加值宣言</a>
运用人脸识别技术、视频审查+语音合成技术等API，解决博物馆受众的残障人士游客存在一些安全隐患、人力资源调配不周等问题。


#### <a name="2">核心价值</a>

为解决博物馆出入游客存在一些安全隐患、人力资源调配不周等问题，我们团队为博物馆推出专属的app，也可应用在博物馆内的一些导览设备上，
通过结合人脸识别技术、视频审查+语音合成技术、计算机影像技术和语音识别技术等。最大程度上解决博物馆的困扰和最大程度满足访客的需求。

#### <a name="3">用户痛点</a>
- (一)博物馆：
1. 访客量多，安全性难以得到保障，再者，在刷身份证入馆的前提下，甚至有盗用身份证的情况。
（解决需求）所以这时候可以使用我们团队所提出的系统，当访客进入博物馆时，在入口处刷身份证并进行人脸验证快速入场，准确核对信息的同时，减少验票和排队的时间
2. 游客可能会有意或无意做出一些不文明行为，需要工作人员进行一定的指导和监督。这就造成工作人员需求量大，且不一定能取到有效的效果。
（解决需求）调用视频审查api，可以全方位并且及时的发现不文明行为，避免造成糟糕的结果，提高了工作效率。 

- (二)游客：
1. 文物进行了解向工作人员进行咨询却因沟通障碍造成困扰和尴尬.通上存在障碍，有时候不懂中文想表达的深层含义，理解起来比较困难。
（解决需求）为博物馆做的电子导览设备或者为移动端所做的小程序中调用语音识别的功能。减少应对不对国家地区人群的翻译解说成本，以及让不同国家地区的参观者可以以自己的母语的方式了解到别国博物馆的文化。
2. 购买周边商品时，存在没有带现金、现在带不够等情况，导致访客不能购买，
（解决需求）：可以通过人脸支付功能实现无现金购物。
3. 独自游览的时候，想要更多的了解一下喜欢的展品，可以通过拍照识别展品的方式，快速的得到该展品的相关信息。



#### <a name="4">人工智能概率性</a>
1.  人脸识别的技术准确性高  
人脸识别API是基于百度海量数据，利用深度学习技术及高精度算法不断迭代模型，准确率业界领先，因此失误率引发用户的负面情绪的可能性一般，用户体验的负面影响压过正面影响的机率较小。  
解决方案：仅使用一款API带来的用户负面情绪风险较大，我们将配合Azure人脸识别及百度的人脸识别多向分析，尽量减少失误率带来的用户负面情绪。  
2.  百度语音合成api技术世界领先  
采用领先国际的流式端到端语音语言一体化建模方法，近场中文普通话识别准确率达98%。中文输入法、搜索模型均可在语音自训练平台上零代码自助训练，上传文本语料即可有效提升业务词汇的识别准确率5-25%。
但如果是中英混杂的对话会出现识别不了的情况，此时我们会提醒用户在使用该功能的时候使用全中或全英的语音及尽量控制在60秒内；出现此情况时，用户体验的负面影响压过正面影响的机率较大。    

#### <a name="5">需求列表</a>
1. 人脸识别api：（验证信息）  
在入闸口增加识别身份证和识别人脸同时进行。验证身份证信息与本人信息是否一致。
2. 视频审查api+语音合成api（排查现场访客是否存在不文明行为）  
针对部分游客的不文明现象，可以通过监控监测到该人的行为超过了预设值，并发出声音播报提醒游客。或者通过手机端（在小程序上）提醒该访客。
3. 语音识别：智能翻译  
通过文字转语音及语音合成完成用户用语言向产品提交问题，无需手打文字。
4. 计算机影像：文物识别_（待做）_  
通过文本分析及文本翻译，将文物中的详情以及文物上的古文和其中的意境解说出来。

### 原型设计  
#### <a name="21">交互及界面设计</a>
 **1.产品架构**  
 
![总览](https://github.com/Eddieda6/museum/blob/master/%E4%BA%A7%E5%93%81%E6%9E%B6%E6%9E%84.png) 

**2.总览**    

![产品架构图](https://github.com/Eddieda6/museum/blob/master/%E6%80%BB%E8%A7%88.png)  


#### <a name="22">信息设计</a>
- 首页搜索页面使用了语音识别API的加值—————  
  减少应对不对国家地区人群的翻译解说成本，以及让不同国家地区的参观者可以以自己的母语的方式了解到别国博物馆的文化。
- 2.1文物识别使用了图片识别api的加值————  
  用户可以当场拍照识别出文物信息，也可以通过回家后把文物重新了解背后的故事。

#### <a name="23">原型文档</a>
[原型文档下载](https://gitee.com/NFUNM172015260/museum/blob/master/api%E5%8D%9A%E5%8D%9A%E7%89%A9%E9%A6%86.rp)  
[原型文档查看](http://nfunm172015260.gitee.io/museum)

#### <a name="24">口头操作与说明</a>  
见产品文档prd

### api

```
{
	"face_num": 1,
	"face_list": [
		{
			"face_token": "86b87dbf1133365b698777b9f4b59f58",
			"location": {
				"left": 816.83,
				"top": 179.93,
				"width": 159,
				"height": 160,
				"rotation": 13
			},
			"face_probability": 1,
			"angle": {
				"yaw": -8.13,
				"pitch": 3.76,
				"roll": 10.2
			},
			"age": 27,
			"beauty": 66.01,
			"expression": {
				"type": "smile",
				"probability": 1
			},
			"face_shape": {
				"type": "oval",
				"probability": 0.65
			},
			"gender": {
				"type": "female",
				"probability": 1
			},
			"glasses": {
				"type": "none",
				"probability": 1
			},
```

