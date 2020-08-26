# NTG_Headphones

Apple的强大勿庸置疑，TWS 蓝牙耳机市场在 AirPods 出现前不温不火，AirPods 出现后整个行业被引爆，“几番仍效法,至今仍领先”。前段时间无意中看到一个新闻说是 Apple 要出一款高阶头戴式耳机 AirPods Studio，不由得想起了两年前给‘牢’厂开发过的一款“胎死腹中”的高阶头戴式耳机。回顾这个项目“作死”的过程，反思过去工作中的不妥之处，探索怎样才能走出一条高阶产品成功开发之路。前事不忘，后事之师。 </br>

立项的时候本来是一小伙伴负责这个项目，但‘牢’厂要求供应商工程师专人专案，不允许工程师同时接多个项目，小伙伴手中已经有个AM61在跑，领导询了一圈没人主动愿接，因为接‘牢’厂的项目受累不讨好,要求高做事累报告多，做好了是应该的，做不好就是背锅侠；再就是会议多，经常性的开到半夜，有的时候晚上一二点拉你电话会议没商量。不晓得怎的就分派到我了，有可能是因为当时手上一个项目在准备量产，正在捣腾的3020又不着急，没啥急的项目。既然领导已经分配，又没什么好的理由来拒绝，只好将就接下来了。</br>

开始整个项目做事的不到十个人，硬件2个，软件1个，电声1个，结构2个，项目2个，测试1个。接手的时候小伙伴将需求包已经拆得七七八八，问小伙伴软件任务要向哪位领导汇报，小伙伴说自己搞定直接对接‘牢’厂。我晕了个去，这是啥节奏！我他妈一杆枪单挑‘牢’厂一群？ 还是‘牢’厂一群群殴我一个？ 你妹！难怪没人主动愿接‘牢’厂的项目。这时我到公司才两月，人都认不全。</br>

一头雾水，晕晕乎乎，把小伙伴给过来的资料啃一遍，整明白牢厂的需求包是个什么产品，前后一个月左右才进入工作状态。把重新整理后的需求发给‘牢’厂项目确认，完了后再跑去云谷‘牢’厂办公室跟工程师对接特性摸底需求，“一杆枪”就这样跟着项目的推进被动进入应答阶段。 </br>

‘牢’厂的尿性两天一报告，三天一汇报，每周一例会，时不时的给你整个额外的啥需求，有时深更半夜拉你电话会议，公司内部每周还有项目例会，项目会议，每周这些屁事搞完，就剩不了几个时间。感觉就是写不完的PPT，画不完的流程图，加上项目工程师均不给力，一浆糊，跟‘牢’厂例会都整不明白需求是什么要做什么应对， 看他们写的项目报告，要气得胸疼，两只都疼，只能将就着每次例会前帮项目完成软件部分的报告，然后项目 CTRL + C / CTRL + V，三不五时回个邮件你还得帮忙拿主意，搬砖的给直接干成项目管理了。
</br>
</br>
****
## 技术规格对比

![huawei_ntg](https://i.loli.net/2020/08/21/SdwEUAFBezZvaf7.png)</br>
</br>

![airpods_sudio](https://i.loli.net/2020/08/21/JtTcD145nOmVPZr.png)</br>
(新闻链接：&ensp;苹果头戴式耳机最新爆料 &ensp;  https://new.qq.com/rain/a/20200808A0JZIY00 )</br>

对比‘牢’厂和 AirPods Studio 的规格，相同之处都要求是High Quality Audio (‘牢’厂HWA), 支持ANC，支持Ear Detection, 这些技术规格用人话讲就是音质要好，指标参数要漂亮，用户体验要佳 ( ANC让用户可以在嘈杂环境下使用，Ear Detect 即戴即使用，都可归为用户体验 )。</br>

技术规格层面上，‘牢’厂的指标参数不比 AirPods Studio 差，策划这个产品的很是牛X, 就等 AirPods Studio 开卖再来PK一下技术指标。</br>

![ntg_spec](https://i.loli.net/2020/08/24/ZtO5g2TwJBEM6xP.png)
‘牢’厂自己拆解需求包最初提出来的技术规格。

### AOV （Always-On Voice)
在应答阶段‘牢’厂在需求包之外会提出许多花样, 要求供应商应答他们再来评估是否要放到需求包中。语音唤醒 (AOV) 和语音控制 ( Voice Command ) 就是其中之一。 </br>

方案选型本不应该是搬砖的事，搬砖的顶多是给建议，做决策至少应该是高一个级别的领导来拍板。项目会议上硬件建议由软件来选型，硬件对这个功能的指标不了解也没接触过。奈何，为了一点碎银子事还得继续做。

语音识别常用的就是所谓的智能音箱，将拾取到的语音送给云端的语音引擎，一个蓝牙耳机要整得这么高大上吗？语音引擎中文做的最好的是科大讯飞，英文非Amazon莫属，内事不决问百度，外事不决问谷歌，度娘、谷大神轮番上阵后，思考一下。</br>

语音引擎，偏重于云端解决语音识别，要是往这两家的方向走跟蓝牙呼叫 Siri 功能有啥区别？‘牢’厂要的是本地语音唤醒与控制，只需要开机/关机/上一曲/下一曲/音量加/音量减/暂停/播放等有限的几个命令，Siri 在关机状态下可开不了机。方向不对，赶紧撤退。</br>

咨询蓝牙芯片供应商，Qualcomm AOV 还在开发中，其它家都回复不支持此功能。AOV 供应商在哪里啊？</br>

没招，度娘、谷大神继续上场，把知名的半导体厂商官网挨个翻个遍，逐个去询信息，还真逮到一家: OnSemi，奥力给！硬件也反馈 Knowles IA610 支持 AOV。有了两家，可以应付‘牢’厂的需求了。 接下来就是一顿常规操作，约供应商介绍产品，讨论技术规格。</br>

供应链回复说OnSemi没用过所以没有联系方式，这个星球上经营理验别具一格的一家半导体供应商竞然不知道，吐血！回到OnSemi官网找到深圳Office的电话打过去，咨询负责的销售的联系方式，一听说是给‘牢’厂做产品，说‘牢’厂他们有专职销售并提供联系方式 (‘牢’厂 VIP 级别的待遇)。拿到联系方式，反手打电话给‘牢’厂工程师，OnSemi销售你们比较熟，帮忙联系下要咨询Voice Command 相关产品，同时发邮件给OnSemi‘牢’厂专职销售咨询工程窗口。就这样跟OnSemi勾搭上了。</br>

搭上‘牢’厂的虎威，找供应商要技术支持通常是一件较容易的事。这些业界牛B的供应商小厂去咨询要支持，随便派个阿猫阿狗代理商 (这已经是不错的待遇，再次一点的就是贸易商) 来了解下有没有商机，很难拿到第一手的技术支持，苦逼的只能把 datasheet 从头翻到尾，再从尾翻到头，或从某个不起眼的notes的字里行间找到你想要的参数。跟‘牢’厂配合这一方面还是比较给力的，有时候‘牢’厂工程师也会主动推荐一些他们认可的供应商资料，对完成应答开发工作会很有帮助。</br>

#### Knowles IA610
Knowles MEMS microphone 在业界那是响当当。Knowles FAE介绍说 IA610 已经跟BES联调成功，申请参考代码，说是这个调试很麻烦云云, 不愿提供 (我勒个去，这哥们硬气！给不给参考代码是你的事，麻不麻烦那是我的事，哥 !)；申请demo平台，也提供不了，给建议去找 BES 申请。一听要找BES申请demo ( BES 是什么尿性？那基本都是有求无应)，赶紧寻求销售的帮助，无助于事。</br>

趁着别人还愿意打发你的时机，赶紧了解了一下 IA610 关注的相关特性。IA610 是基于关键词的特征值语音识别算法，最多可以植入3段语音，中文3段语音总共不能超过10个字(印象中是这个数据)，唤醒功耗 (识别到关键词后唤醒并给出中断信号这整个过程) 大约电流3--4mA, 唤醒后提供一个中断信号给外部系统。关键词需要在 Knowles 工厂生产前植入，用户无法更改。</br>

了解了，告辞!</br>

![ia610_current](https://i.loli.net/2020/08/22/oDtdxqERjwp5JU3.png) </br>
_IA610_Figure1_

![ia610_int](https://i.loli.net/2020/08/22/DS9pzQyH8qRJen7.png) </br>
_IA610_Figure2_

#### OnSemi Sound Solution
OnSemi 有两款产品支持 voice trigger, LC823450 和 Belasigna R281。
##### LC823450
LC823450是 OnSemi 音频处理系统 LSI，支持 voice trigger 和 voice command，还集成蓝牙 PHY (功能强大，再凑个蓝牙RF就是一颗集成蓝牙功能的完整本地语音控制播放器 SoC )。联系上海FAE申请 demo, 反馈信息回来 demo 在福州 AE 部门，要跟 AE 部门协调，几番邮件往来，终究也没能拿到 demo。评估工作还是要继续，只好继续骚扰上海 FAE 寻求帮助，终于拿到了心心念念的数据。</br>

![lc823450_current](https://i.loli.net/2020/08/22/bzTLU4GjKBCaWD8.png)
</br>

voice trigger 状态下的功耗还是蛮大的，估计再怎么优化也还是要到 mA 级别，蓝牙耳机产品上这么大功耗够呛。后来 AE 部门的工程师带着他们日本的同事有过来交流，闲聊中得知这颗芯片是日本那边设计的，三星出过一款录音笔是用这颗芯片做的，在国内业务端也不清楚应用方向在哪里，所以不受总部重视。这玩意仅适合于对功耗不敏感的产品，耳机产品用不起。

![lc823450_feature](https://i.loli.net/2020/08/26/mDc9ZdtI2LRKBuk.png)

##### Belasigna R281
Belasigna R281 是基于声纹的关键词语音触发独立方案，兼容模拟和数字麦克风, 检测经过用户训练的触发词组(关键词, 可以有3组不同的关键词)，检测到该触发词组时发出一个唤醒信号。用户可重复设置 3 段语音，3 段语音总共时长不能超过 1.5s。</br>

![r281_current](https://i.loli.net/2020/08/22/xlwNPJSbCjAkoet.png)
</br>

IA610 采用语言模型，需要采集大数量人群的关键词语音， 然后提取出来特征值 (特定文字) 建立声学模型，如果唤醒词与声学模型匹配上，那么设备唤醒。假设你在用蓝牙耳机接电话的应用场景，旁边别人说关机，那是不是我的蓝牙耳机也要关机？都不用去评估唤醒率/误唤醒/响应时间/功耗这些参数，我脑子瓦特了才会采用这种方案，NG。</br>

R281 基于声纹，在用户训练触发短语时提取用户的唤醒词的音素序列建立声学模型，唤醒词与音素序列匹配上，则设备唤醒输出唤醒信号。唤醒词可以是任何的短语，且不与语言语音相关。‘牢’厂要求的是八国语言，那这种不与语言相关且仅是单个用户唤醒词才能唤醒设备的方案，就是我心目中想要的解决方案。R281 demo 做成了usb dongle 形式使用相当方便，插入电脑 usb 接口打开应用程序就可评估。当我在‘牢’厂办公室演示的时候，这帮货还是比较惊羡的，在办公室的场景下训练时说话声音稍微大一点，测试十次有八九次是成功的，再一个功耗能控制到 uA 级别出乎意外。</br>

在系统层面，如果‘牢’厂要求支持 AOV 与 Voice Command, 以手上现有的供应商资源只能将 LC823450 当作MCU (大材小用)，开发工作量可能会很大 (以 LC823450 芯片的复杂程度估计不是那么容易上手)。</br>

![aov_flow](https://i.loli.net/2020/08/26/aNY2U5GA3FRtsh9.png)

最终‘牢’厂还是放弃了 AOV 与 Voice Command, 但还是 mark 一下: 从功能上考量，AOV 与 Voice Command 在耳机产品上没有必需存在的意义; 从功耗上考量，在电池能量密度没有大的技术突破前，耳机还没奢侈到这种地步。</br>

### DSD
DSD 功能是‘牢’厂在需求包里提出来的需求，可能是 CM21 (CM21的产品策划必需要点个赞) 的成功让‘牢’厂意识到这个市场的具大需求。在需求对接的时候‘牢’厂项目提出来必需是 native DSD, 先找到解决方案再来看‘牢’厂要求的摸底特性。</br>
在 DSD Player 市场， 见的多的方案是 xMOS 的，查阅过资料后觉得比较麻烦：xMOS 方案仅是将 USB DSD 音频流转换成 PCM DSD音频流，后面还要挂一颗支持PCM DSD音频流，换句话来说 xMOS 方案仅负责将 USB 音频格式的 DSD data 翻译成 PCM 音频流, 虽然 xMOS 官网上提供参考代码，就我一杆枪去做这个集成工作这是给自己找麻烦，BIG TROUBLE，打个问号先。 </br>
这其间‘牢’厂工程师介绍了另外一家供应商 BigSound, 一通联系沟通之后，拿到规格书浏览一遍之后，决定先放一边仅作参考。‘牢’厂要求是 native DSD64/128, 这一点就满足不了。但评估工作还是要做，demo 板还得要申请。这就是给‘牢’厂做项目的痛苦之处，就算被否的方案你也要出评估报告说明为什么不行，除了不行之点外其它性能能达到什么程度。写报告的时间比我搬砖的时间多三倍都不止。

![bcc2102_format](https://i.loli.net/2020/08/26/FvNMqKEDbmVXgou.png)</br>
_BCC2102_ </br>

还是参考 CM21 的解决方案，‘牢’厂既然已经大批量开卖了，有 bug 估计也能接受。

### OTA 与 双备份


### BES2300Y
蓝牙音频传输做死了SNR也不会超过75dB，High Quality Audio的SNR下限不会低于90dB，‘牢’厂就直接给出了SNR不低于110dB。</br>


‘牢’厂CM21

合理搞钱，服务社会。

各种姿势跪舔都不如给出最优的产品达成客户的目标。
一杆枪其实也没啥不适应，天高任鸟飞。

正常的情况下方案选型的最小系统有两个角色：建议者(写代码的)和决策者(产品经理)。领导们在开会时一个个都说软件我不了解啊，担当不了 SE 这个角色。听说 AM61 曾经‘牢’厂项目因为不满意项目工程师的工作投诉到大老板那里要求换人，令领导们心有余悸。有天开例会，就我和老板两个人先到，老板对我突然蹦出来一句：这个项目如果失败，软件要承担主要责任。有没有碰到错题，还要划对勾的违心感。项目还没开始就想着甩锅了！什么样的老板带什么样的兵。当时一下没反应过来，想了想，我说按现在的软件系统规划，软件不会是瓶颈。虽然还在应答阶段，对‘牢’厂这个产品摸爬滚打下来软件大体框架已经有了几分把握，背锅侠，不存在的。</br>
