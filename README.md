# NTG_Headphones

Apple的强大勿庸置疑，TWS 蓝牙耳机市场在 AirPods 出现前不温不火，AirPods 出现后整个行业被引爆，“几番仍效法,至今仍领先”。前段时间无意中看到一个新闻说是 Apple 要出一款高阶头戴式耳机 AirPods Studio，不由得想起了两年前给‘牢’厂开发过的一款“胎死腹中”的高阶头戴式耳机。回顾这个项目“作死”的过程，反思过去工作中的不足之处，探索如何成为高效创新开发团队。前事不忘，后事之师，抛个砖，引个玉。 </br>

立项的时候本来是一小伙伴负责这个项目，但‘牢’厂要求供应商工程师专人专案，不允许工程师同时接多个项目，小伙伴手中已经有个FreeLace在跑，领导询了一圈没人主动愿接，因为接‘牢’厂的项目受累不讨好,要求高做事累报告多，做好了是应该的，做不好就是背锅侠；再就是会议多，经常性的开到半夜，有的时候晚上一二点拉你电话会议没商量。不晓得怎的就分派到我了，有可能是因为当时手上一个项目在准备量产，正在捣腾的3020又不着急，没啥急的项目。既然领导已经分配，又没什么好的理由来拒绝，只好将就接下来了。</br>

开始整个项目做事的不到十个人，硬件2个，软件1个，电声1个，结构2个，项目2个，测试1个。接手的时候小伙伴将需求包已经拆得七七八八，问小伙伴软件任务要向哪位领导汇报，小伙伴说自己搞定直接对接‘牢’厂。我晕了个去，这是啥节奏！我他妈一杆枪单挑‘牢’厂一群？ 还是‘牢’厂一群群殴我一个？ 你妹！难怪没人主动愿接‘牢’厂的项目。</br>

一头雾水，晕晕乎乎，把小伙伴给过来的资料啃一遍，整明白牢厂的需求包是个什么产品，前后一个月左右才进入工作状态。把重新整理后的需求发给‘牢’厂项目确认，完了后再跑去云谷‘牢’厂办公室跟工程师对接特性摸底需求，“一杆枪”就这样跟着项目的推进被动进入应答阶段。 </br>

‘牢’厂的尿性两天一报告，三天一汇报，每周一例会，时不时的给你整个额外的啥需求，有时深更半夜拉你电话会议，公司内部每周还有项目例会，项目会议，每周这些屁事搞完，就剩不了几个时间。感觉就是写不完的PPT，画不完的流程图，加上项目工程师均不给力，一浆糊，跟‘牢’厂例会都整不明白需求是什么要做什么应对， 看他们写的项目报告，要气得胸疼，两只都疼，只能将就着每次例会前帮项目完成软件部分的报告，然后项目 CTRL + C / CTRL + V，三不五时回个邮件你还得帮忙拿主意，搬砖的给直接干成项目管理了。</br>
***
## Specifications
<details> </br>

![huawei_ntg](https://i.loli.net/2020/08/21/SdwEUAFBezZvaf7.png)</br>
</br>

![airpods_sudio](https://i.loli.net/2020/08/21/JtTcD145nOmVPZr.png)</br>
(新闻链接：&ensp;苹果头戴式耳机最新爆料 &ensp;  https://new.qq.com/rain/a/20200808A0JZIY00 )</br>

对比‘牢’厂和 AirPods Studio 的规格，相同之处都要求是High Quality Audio (‘牢’厂HWA), 支持ANC，支持Ear Detection, 这些技术规格用人话讲就是音质要好，指标参数要漂亮，用户体验要佳 ( ANC让用户可以在嘈杂环境下使用，Ear Detect 即戴即使用，都可归为用户体验 )。</br>

技术规格层面上，‘牢’厂的指标参数不比 AirPods Studio 差，策划这个产品的很是牛X, 就等 AirPods Studio 开卖再来PK一下技术指标。</br>

![ntg_spec](https://i.loli.net/2020/08/24/ZtO5g2TwJBEM6xP.png)
_‘牢’厂自己拆解需求包最初提出来的技术规格_

方案选型本不应该是搬砖的事，搬砖的顶多是给建议，选型决策至少应该是高一个级别的领导来拍板。领导们在开会时一个个都说软件我不了解啊，担当不了 SE 这个角色。听说曾经‘牢’厂项目因为不满意项目工程师的工作投诉到大老板那里要求换人，令领导们心有余悸。有天开例会，就我和老板两个人先到，老板对我突然蹦出来一句：这个项目如果失败，软件要承担主要责任。有没有碰到错题，还要划对勾的违心感。项目刚开始就想着甩锅了！当时一下没反应过来，沉默了一下，我说按现在的软件系统规划，软件不会是瓶颈。对‘牢’厂这个产品需求摸爬滚打下来软件大体框架已经有了几分把握，背锅侠，不存在的。为了一点碎银子还是面对疾风吧！</br>
</details>

### AOV （Always-On Voice)
<details> </br>
在应答阶段‘牢’厂在需求包之外会提出许多花样, 要求供应商应答他们再来评估是否要放到需求包中。语音唤醒 (AOV) 和语音控制 ( Voice Command ) 就是其中之一。 </br>

语音识别常用的就是所谓的智能音箱，将拾取到的语音送给云端的语音引擎，一个蓝牙耳机要整得这么高大上吗？语音引擎中文做的最好的是科大讯飞，英文非Amazon莫属，内事不决问百度，外事不决问谷歌，度娘、谷大神轮番上阵后，思考一下。</br>

语音引擎，偏重于云端解决语音识别，要是往这两家的方向走跟蓝牙呼叫 Siri 功能有啥区别？‘牢’厂要的是本地语音唤醒与控制，只需要开机/关机/上一曲/下一曲/音量加/音量减/暂停/播放等有限的几个命令，Siri 在关机状态下可开不了机。方向不对，赶紧撤退。</br>

咨询蓝牙芯片供应商，Qualcomm AOV 还在开发中，其它家都回复不支持此功能。AOV 供应商在哪里啊？</br>

没招，度娘、谷大神继续上场，把知名的半导体厂商官网挨个翻个遍，逐个去询信息，还真逮到一家: OnSemi，奥力给！硬件也反馈 Knowles IA610 支持 AOV。有了两家，可以应付‘牢’厂的需求了。 接下来就是一顿常规操作，约供应商介绍产品，讨论技术规格。</br>

供应链回复说OnSemi没用过所以没有联系方式，这个星球上经营理验别具一格的一家半导体供应商竞然不知道，吐血！回到OnSemi官网找到深圳Office的电话打过去，咨询负责的销售的联系方式，一听说是给‘牢’厂做产品，说‘牢’厂他们有专职销售并提供联系方式 (‘牢’厂 VIP 级别的待遇)。拿到联系方式，反手打电话给‘牢’厂工程师，OnSemi销售你们比较熟，帮忙联系下要咨询Voice Command 相关产品，同时发邮件给OnSemi‘牢’厂专职销售咨询工程窗口。就这样跟OnSemi勾搭上了。</br>

搭上‘牢’厂的虎威，找供应商要技术支持通常是一件较容易的事。这些业界牛B的供应商小厂去咨询要支持，随便派个阿猫阿狗代理商 (这已经是不错的待遇，再次一点的就是贸易商) 来了解下有没有商机，很难拿到第一手的技术支持，苦逼的只能把 datasheet 从头翻到尾，再从尾翻到头，或从某个不起眼的notes的字里行间找到你想要的参数。跟‘牢’厂配合这一方面还是比较给力的，有时候‘牢’厂工程师也会主动推荐一些他们认可的供应商资料，对完成应答开发工作会很有帮助。</br>

#### Knowles IA610
<details></br>
Knowles MEMS microphone 在业界那是响当当。Knowles FAE介绍说 IA610 已经跟BES联调成功，申请参考代码，说是这个调试很麻烦云云, 不愿提供 (我勒个去，这哥们硬气！给不给参考代码是你的事，麻不麻烦那是我的事，哥 !)；申请demo平台，也提供不了，给建议去找 BES 申请。一听要找BES申请demo ( BES 是什么尿性？那基本都是有求无应)，赶紧寻求销售的帮助，无助于事。</br>

趁着别人还愿意打发你的时机，赶紧了解了一下 IA610 关注的相关特性。IA610 是基于关键词的特征值语音识别算法，最多可以植入3段语音，中文3段语音总共不能超过10个字(印象中是这个数据)，唤醒功耗 (识别到关键词后唤醒并给出中断信号这整个过程) 大约电流3--4mA, 唤醒后提供一个中断信号给外部系统。关键词需要在 Knowles 工厂生产前植入，用户无法更改。</br>

了解了，告辞!</br>

![ia610_current](https://i.loli.net/2020/08/22/oDtdxqERjwp5JU3.png) </br>
_IA610_FIGURE1_

![ia610_int](https://i.loli.net/2020/08/22/DS9pzQyH8qRJen7.png) </br>
_IA610_FIGURE2_
</details>

#### OnSemi Sound Solution
<details> </br>

OnSemi 有两款产品支持 voice trigger, LC823450 和 Belasigna R281。
##### LC823450
LC823450是 OnSemi 音频处理系统 LSI，支持 voice trigger 和 voice command，还集成蓝牙 PHY (功能强大，再凑个蓝牙RF就是一颗集成蓝牙功能的完整本地语音控制播放器 SoC )。联系上海FAE申请 demo, 反馈信息回来 demo 在福州 AE 部门，要跟 AE 部门协调，几番邮件往来，终究也没能拿到 demo。评估工作还是要继续，只好继续骚扰上海 FAE 寻求帮助，终于拿到了心心念念的数据。</br>

_LC823450_POWER_CONSUMPTION_
![lc823450_current](https://i.loli.net/2020/08/22/bzTLU4GjKBCaWD8.png)</br>

评估 AOV 除了芯片的功耗，加上 mic 处于常供电状态下的功耗。voice trigger 状态下的功耗还是蛮大的，估计再怎么优化也还是要到 mA 级别，蓝牙耳机产品上这么大功耗够呛。后来 AE 部门的工程师带着他们日本的同事有过来交流，闲聊中得知这颗芯片是日本那边设计的，三星出过一款录音笔是用这颗芯片做的，在国内业务端也不清楚应用方向在哪里，所以不受总部重视。功耗不敏感的场合比较合适。</br>

_LC823450_FEATURE_SUMMARIZATION_</br>
![lc823450_feature](https://i.loli.net/2020/08/26/auNE7A9WtQq4iMZ.png)</br>
</br>
##### Belasigna R281
Belasigna R281 是基于声纹的关键词语音触发独立方案，兼容模拟和数字麦克风, 检测经过用户训练的触发词组 (最多3组不同的关键词)，检测到该触发词组时发出一个唤醒信号。用户可重复设置 3 段语音，3 段语音总共时长不能超过 1.5s。</br>

_R281_POWER_CONSUMTION_
![r281_current](https://i.loli.net/2020/08/22/xlwNPJSbCjAkoet.png)</br>

IA610 采用语言模型，需要采集大数量人群的关键词语音， 然后提取出来特征值 (特定文字) 建立声学模型，如果唤醒词与声学模型匹配上，那么设备唤醒。假设你在用蓝牙耳机接电话的应用场景，旁边别人说关机，那是不是我的蓝牙耳机也要关机？都不用去评估唤醒率/误唤醒/响应时间/功耗这些参数，我脑子瓦特了才会采用这种方案，NG。</br>

R281 基于声纹，在用户训练触发短语时提取用户的唤醒词的音素序列建立声学模型，唤醒词与音素序列匹配上，则设备唤醒输出唤醒信号。唤醒词可以是任何的短语，且不与语言语音相关。‘牢’厂要求的是十国语言，那这种不与语言相关且仅是单个用户唤醒词才能唤醒设备的方案，就是我心目中想要的解决方案。R281 demo 做成了usb dongle 形式使用相当方便，插入电脑 usb 接口打开应用程序就可评估。当我在‘牢’厂办公室演示的时候，这帮货还是比较惊羡的，在办公室的场景下训练时说话声音稍微大一点，测试十次有八九次是成功的，再一个功耗能控制到 uA 级别出乎意外。</br>
</details>
</br>
在系统层面，如果‘牢’厂要求支持 AOV 与 Voice Command, 以手上现有的供应商资源只能将 LC823450 当作MCU (大材小用)，开发工作量可能会很大 (以 LC823450 芯片的复杂程度估计不是那么容易上手)。</br>
</br>

_AOV&VOICE_COMMAND_FUNCTION_FLOW_CHART_
![aov_flow](https://i.loli.net/2020/08/26/aNY2U5GA3FRtsh9.png)</br>
</br>
最终‘牢’厂还是放弃了 AOV 与 Voice Command, 但还是 mark 一下: 从功能上考量，AOV 与 Voice Command 在耳机产品上对普通消费者没有必需存在的意义; 从功耗上考量，在电池能量密度没有大的突破前，有点膨胀了。</br>

</details>

### DSD & USB Audio
<details></br>
<!-- <summary> <mark> <font color = blue> 点击查看具体内容 </font> </mark> </summary> </br>  -->

DSD 功能是‘牢’厂在需求包里提出来的需求，可能是 CM21 (CM21的产品策划必需要点个赞) 的成功让‘牢’厂意识到高清音频市场的巨大需求。手机原生支持 DSD 64/128 抢掉千元 DSD 播放器市场，顺带收割一波信仰，这个产品策划有想法。在需求对接的时候‘牢’厂项目强调必需是 native, 先找到解决方案再来看‘牢’厂要求的摸底特性。</br>

在 DSD Player 市场， 见的多的方案是 xMOS 的，查阅过资料后觉得比较麻烦：xMOS 方案是将 USB DSD 音频流解码成 PCM 音频流输出，可以支持到 DSD 512，虽然 xMOS 官网上提供参考代码，但它用的是一套 xMOS 自己搞的一套编译环境，就我一杆枪去做这个集成工作估计是给自己找麻烦，BIG TROUBLE，打个问号先。 </br>

BES2300 也可以支持 DSD 64/128， 但是它是软解，这与‘牢’厂要求的 DSD native 要求不符 (native 意味着一定是硬解)，另一个问题是仅支持 UAC2.0, 在 WIN7 下兼容性问题解决不了，但是单芯片方案在软硬件开发上会省事很多，至少整体软件框架原厂应该是有的，不用在软件框架上花太多精力。有线通话功能咨询 BES 回复可以支持，需要修改 SDK。demo 板搞起。

这其间‘牢’厂工程师介绍了另外一家供应商 BigSound, 一番联系沟通之后拿到规格书, 浏览一遍之后，决定先放一边仅作参考, 缺点是不符合 native 的要求。但评估工作还是要做，demo 板也还得要申请。

这就是给‘牢’厂做项目的痛苦之处，你需要准备两个以上的方案供他们评估，就算你认为不合适的方案你也要出评估报告说明为什么不行，除了不行之点外其它性能能达到什么程度，来证明你不是口嗨，是真真确确有做评估，所以造成写报告的时间比搬砖的时间多三倍不止。

![bcc2102_format](https://i.loli.net/2020/08/26/FvNMqKEDbmVXgou.png)</br>
_BCC2102_FEAURE_ </br>

还是参考 CM21 的解决方案，‘牢’厂既然已经大批量开卖了，有 bug 估计也能接受。从硬件那里拿到datasheet, 再跟 Savitech FAE 确认之后决定就用它了。决定选用 SA9312L 的另一个原因是它支持 UAC 1.0 & 2.0，WIN10 原生支持 UAC2.0，MAC OS 10.0 以上版本也是同样原生支持 UAC 2.0，这就解决了 USB Audio 在其它系统下的兼容性的问题。支持 IIC 更新 firmware。</br>
(PS：MAC OS 10.0 以上版本原生支持 UAC 2.0 出处待考证，时间过去太久了，以前的开发笔记上没有查到当初的记录)</br>

![sa9312l_feature](https://i.loli.net/2020/08/26/oXwHkFE8sY2PB34.png)</br>
_SA9312L_FEATURE_

DSD 解码方案差不多有了，剩下就是音频输出端的 DAC 选型。DAC 行业内能选的就那么几家，在各自的网站上一筛选，我倾向于 CS43131 (带 SRC)， 硬件倾向于 AK4377。 当我们还在准备比较两家的性能时，‘牢’厂传来弃美方案，这下好了，不用选了直接评估 AK4377。

接下来就是一顿操作猛如虎，按照‘牢’厂要求测试然后输出报告。因为手上没有 MAC 设备，在 VMWare 虚拟机上安装 MAC OS 10.12 版本能识别到设备但无法传输声音，BES2300 也出现同样问题，咨询 BES 杳无音信，怀疑设备端要支持Apple USB IAP 认证, 特性摸底就先忽略了这个问题。</br>

支持 DSD 其实对硬件要求更高，对软件来说找到可行的方案且能支持 USB HID 就差不多完成了工作，硬件往往因为实际产品音频指标参数不达标而卡壳。为了满足 DSD 超高的音频指标要求，外围硬件线路通常具备很强的驱动能力，又因为 DSD 音频信号幅值peak-peak通常为5V，所以输出功率会很大，Cirrus Logic 工程师调侃称之为行走的外放蓝牙耳机。


<!--
_AK4497_BLOCK_DIAGRAM_ </br>
![ak4497_block](https://i.loli.net/2020/08/27/EycgLdeqSp5WFsA.png)</br>
</br>
_CS43131_BLOCK_DIAGRAM_
![cs43131_block](https://i.loli.net/2020/08/27/Ppzye9mSaXGUICV.png)

DSD 音频流不带音量信息，而且 DSD 音频流解码输出后会比其它格式的音频音量要低 3dB (印象中是这么多，如果有错麻烦指正)，而且支持 DSD 的硬件线路会很复杂， 。上图如果输入的 DSD 音频流走红圈中的音频路径，就是 native DSD, 否则就是DoP。</br>

_AK4490_ANALOG_CHARACTERISTICS_ </br>
![ak4490_analog_param](https://i.loli.net/2020/08/27/vh4KudQ31egWYZD.png)</br>

</br>

![ak4497_dsd_sn](https://i.loli.net/2020/08/27/tWbjSraNARX7yHo.png)</br>

再来看看这些DAC的可怖功耗 </br>

_AK4497_POWER_SUPPLY_ </br>
![ak4497_pwr_supply](https://i.loli.net/2020/08/27/16GFiDh854XrJ7m.png)</br>
-->
</details>

### TOUCH & PROXIMITY
<details>
</br>
触摸与佩戴在需求包里‘牢’厂没有明确的定义，开发最怕的就是这种看起来没有要求的需求，单边触摸还是双边触摸，要不要支持滑动，连续滑动，多点触碰，单边佩戴检测还是双边佩戴检测，都没有定义，‘牢’厂项目要求摸底竟品和供应商产品规格再来定需求。</br>
</br>
触摸与佩戴芯片查过很多供应商的资料，都不令人满意，最后还是求助于‘牢’厂开放资源，拿到了 AZOTEQ 的联系方式。把PXC 550， WH-1000XM3，QC 35 II 等一堆耳机申请回来，把 UI 操作和供应商产品规格整理完成发给‘牢’厂，加上‘牢’厂自己也摸底评估，最后定义单边触摸，双边佩戴，支持连续滑动与多点触摸 (连续滑动控制音量，多点触摸检测手捂动作切换监听模式)。</br>
</br>
在啃过 AZOTEQ 推荐的 IQS572 与 IQS620 规格书，demo 板也都评估过后，我是比较满意 AZOTEQ 的方案，调试有 GUI 工具，灵敏度软件可调，稳定性从 GUI 工具上判断也没遇到什么异常。规格书 IQS572 与 IQS620 所标明的功耗如果无误，我在想是否可以实现佩戴即开机功能。头戴耳机在佩戴过程中通常先是双手握住听筒(握住听筒不一定会有触摸动作)，然后再佩戴，握住听筒时通过触摸芯片接近感应中断唤醒系统，正确佩戴识别后进入开机流程，不用按实体键开机再去佩戴。我戴上耳机是用来装B的不是用来听歌的，杠精请绕道。IQS620 内置的是 ROM, 上电使用前要做初始化。</br>
</br>

![iqs572_feature](https://i.loli.net/2020/08/28/zFs27Yx9bJDlpL1.png)</br>
_IQS572_MAIN_FEATURE_

![iqs620_feature](https://i.loli.net/2020/08/29/7KB3XudYZMgCiTP.png)</br>
_IQS620_FEATURE_

滑动触摸 (finger gesture) 牵涉到移动方向的判断，位置坐标的计算是相对于原点坐标计算而来，这个原点坐标对于 IQS572 而言是一个绝对坐标，在触摸板加工出来之后这个原点坐标和其对应的 X/Y 轴就已经固定。使用者在佩戴耳机时各种角度都可能会出现，不会是一种理想的正戴在头顶的这种方式，而如果要得到与物理水平面的坐标位置来解决滑动触摸方向问题，需要增加 G-sensor。AZOTEQ 建议将角度偏差设为26度左右，在给‘牢’厂在出结构样机时试用过触摸功能后，认为还比较理想，就没有在这个功能上继续纠缠。阿弥陀佛，逃过一劫！IQS572 触摸算法是 AZOTEQ 设计，应用端仅需要在它中断触发外部控制器时去读取数据做判断，从 IQS572 读取位置坐标再通过 G-sensor 的数据转换成物理水平位置，手势动作的算法就变成要自己去设计，这是我一杆枪绝对不想去面对的情况。 </br>

第一次做结构样板时因‘牢’厂要求触摸介质用的是蓝宝石玻璃，触摸手感确实很好，最终还是抵不过成本压缩改成了普通塑料片，质感差的不是一星半点。</br>
</details>

### ANC & ENC
<details></br>
ANC & ENC 的需求同样在需求包里没有明确，‘牢’厂要求把能找到的方案都找出来，分析评估。在双MIC/三MIC一轮分析评估过后，‘牢’厂明确上下行都需要是3-mic降噪。因为以前用过 CXD3781 所以就联系了 Sony 半导体部门拿到了 CXD3782 的资料，绿岛那边 Cirrus Logic 听说‘牢’厂新开头戴耳机项目，主动找过来介绍 CS47L5x。BES 原厂的 ANC 方案‘牢’厂在评估过后弃用了，同样因为弃美方案的原因，ADI 和 Cirrus Logic 的方案最终都不能用， 就只剩下了 CXD3782。</br>
</br>
虽然 Sony AE 声称 WH-1000XM3 用的就是 CXD3782，但是将 CXD3782 规格书从头翻到尾也没找到关于数据安全加载的说明。芯片工作在某一固定 EQ 下时再去调节某一频点的参数可能会带来冲击声或其它噪音，数据安全加载就是为了解决这个问题。WH-1000XM3 自适应降噪功能如何实现的就不得而知了。</br>
</br>
<!--
![adau1701_safeload](https://i.loli.net/2020/08/29/5MSvGVrckE8qK2D.png)</br>
-->

![adau1401a_safeload](https://i.loli.net/2020/08/29/cGEeD2KhIzbFMTS.png)</br>
_ADAU1701_SAFELOAD_LOGIC_

即使是 ADI 的芯片有 safeload 机制，但在播放标准测试信号如 100Hz/1kHz 等时，调节 EQ 参数也还是会有轻微的 冲击声。</br>

在评估过程中发现 CXD3782 在 GUI EQ 调试界面下 gain 值的调整区间只有 -20 -- 20dB, 超过此范围就无法显示，会不会引起数值溢出也没能确认。电声实际测试时降噪深度只能达到到 26dB 左右 (印象中是差不多是这么多), ‘牢’厂项目包括后台的可能是做 ANC 算法的一直追问为什么只能做到26dB, 这种问题就不是做应用开发的能回答的问题，只能求助原厂本部。个人认为降噪深度在头戴耳机上能做到 20dB 以上已经可以算是优秀，降噪深度越深，在轻微噪音场合负压感越强，而且头戴耳机天然的就有被动降噪效果 (这一点与手机不同)，真要把外部噪音隔决反倒会带来安全性问题。降噪深度与头戴耳机的关联性，这个话题后来再未深入讨论过，蛮遗憾的。</br>

ENC 开始是直接用 BES 的算法评估，因 3-mic 主频要跑到 208M，‘牢’厂要求测试跑 208M 的系统稳定性，咨询 BES 稳定性的验证策略， 没有，MMP! 没招了只能硬着头皮直接测通话。移植3-mic算法后测了三天拔打/接听电话，通话时长随机，最长的一次估计是有两小时，测试次数 100 次是有的，还好 BES2300 这次比较给力，没遇到什么异常，稳定性看起来没有问题，直接输出测试报告给‘牢’厂。双MIC/三MIC 在测试评估过后‘牢’厂不满意降噪效果，联系 BES 上海那边说是要拿样机来调试，样机寄过去后就没有了后续。还好，BES 方案支持第三方算法，找了三家供应商，弃美方案原因去掉两家，剩下一家，还好是国产算法而且降噪效果‘牢’厂也比较满意。</br>

‘牢’厂要求支持有线通话，到底是外加 ENC 芯片还是通过软件切换到 BES2300 通话链路来处理，在这个地方犯难了，主要考虑是外加 ENC 成本增加与硬件线路复杂主板堆叠能否放得下。硬件小伙伴也没有更好的建议，只能放到系统设计时再考虑。</br>

</details>

### BMS
<details></br>
电源管理一开始没有打算用国产方案，十二月份的时候‘牢’厂提出要有国产备选方案，找‘牢’厂开放资源推荐了 SY6970。看了下 SY6970 的规格书，有电源路径管理 (power path management)，功耗也能接受，性能也能满足项目的需求，并且‘牢’厂其它产品上用过，一月份确定要用国产方案的时候就直接用上了。</br>
</br>
硬件是直接用上了，但评估工作一个也不能少，demo 申请还是要来一波。‘牢’厂指定的 660mAH/4.4V 电池虽然不喜，但人家是甲方, 评估下来 DSD 功能下的工作时长会有风险。‘牢’厂项目给出的原因是电池认证需要 6--8 个月，时间不允许，只能用现有的已认证的电池。在春节前的项目进度表上量产时间已经延到了 11 月份，重新评估需求定制电池去做认证时间完全充裕。</br>
</br>
‘牢’厂要求二段式充电 1.1C & 0.7C，demo 板上验证在充电状态下充电电流可配置，对软件来说就没有问题了。SY6970 不支持快充，shipping mode 下的功耗 15 uA, 有点大，国产芯片还要继续努力，对标 TI 应是我们的目标。</br>

电源管理容易出问题的是充电设备兼容性，有可能没有漏掉设备但是漏掉了某种应用场景。新产品开发过程中没有办法把应用场景一次性全部覆盖到，都是摸着石头过河，遇到问题再去解决问题。</br>

送给‘牢’厂的样机连接手机边播音乐边充电测试充电底噪的时候在静音房听出来有明显现嘀嘀异响，收到‘牢’厂的反馈觉得有点诧异，不应该出现吧？查资料，测信号，在代码里添加读取寄存器。</br>
</br>
![BC1.2_FINAL_sdp](https://i.loli.net/2020/09/05/vmKZuPpVHfEzrh2.png) </br>
_BC1.2_FINAL_ </br>
</br>
![sy6970_reg0B](https://i.loli.net/2020/09/05/lH1fVIthDLzByXQ.png)</br>
_SY6970_FIGURE1_ </br>
</br>
![sy6970_reg00](https://i.loli.net/2020/09/05/Sg47DuEmjLo2UpV.png)</br>
_SY6970_FIGURE2_ </br>
</br>
![sy6970_reg13](https://i.loli.net/2020/09/05/1uJtjCZymfsYzBn.png)</br>
_SY6970_FIGURE3_ </br>
</br>
![sy6970_dynamic_pwrms](https://i.loli.net/2020/09/05/48dhjxzYwMVX26A.png)</br>
_SY6970_FIGURE4_ </br>
</br>
![sy6970_battery](https://i.loli.net/2020/09/05/CbJkcBNyK2MdZRG.png)</br>
_BATTERY_VOLTAGE_FIGURE_ </br>
</br>
在配置充电策略的时候手头上的充电器都没有被 SY6970 识别为 SDP (设备兼容性当时是在 demo 板上调试的，兼容性调试完成后也没有在自己的板上重新验证)，就漏掉了 SDP 最大 100mA 充电电流的应用场景，也有可能是在调试的时候没有把电池耗尽去做充电测试而漏掉了这个应用场景。充电策略在软件处理流程上是忽略 SY6970 识别到的设备的 IINlim (SY6970_FIGURE2)，根据当前的电池电压强制将最大充电电流设为 1.1C 或 0.7C, 充电电流就可能会远大于 SY6970 识别到的设备输入最大电流限制，触发了 SY6970 的保护机制将最大充电电流重设为 100mA, 软件流程定时检测，发现设置的最大充电电流低于 1.1C 或 0.7C 又会将最大充电电流设为 1.1C 或 0.7C， 就出现了电池电压波动的情形 (BATTERY_VOLTAGE_FIGURE), 这个波动信号藕合到了喇叭输出线路上就出现了噪音 (好死不死的喇叭线路靠近充电线路 :cold_sweat:)。</br>

在配置充电策略的时候一定要用自己的板做完整的充放电测试，另外就是严谨一点把电池正极和充电设备供电正极挂上示波器探头。</br>
</details>

### HWA
<details></br>

HWA 我更希望‘牢’厂称之为 LHDC, 瓜田李下,‘牢’厂应该要有这种觉悟；合理搞钱，服务社会，也应具备这样的格调。之前的月亮事件确实是被恶心到了，Robin 算是前车之鉴 (Jack 福报论，Pony 南山必胜客，仅是没有 Robin 的竞价排名那么大的社会破坏力)。</br>

跟供应商询了一圈，支持 LHDC 的Qualcomm 8675 因功耗太大被硬件否了，QCC系列 Qualcomm 代理商回复要 Q1 才能完成集成工作，还特意咨询过 Savitech SA9721，因为市场上基本没有客户用过，也被否了，现成能实际评估的就只剩下 BES2300。</br>

FreeLace 立项之初‘牢’厂也是要求要支持LHDC，因为各种原因最终产品发布的时候取消掉了。虽然小伙伴们之前已经做过一些验证工作，但是没有完整的测试数据与评估报告，想偷个懒都不给机会，重头开始吧。</br>

LLAC 最初在规格定义的时候大家还有讨论过，因为不支持白金标后来就没有多做讨论，另一个原因是强调要把 LLAC 加入评估的‘牢’厂相关人员后来退出了这个项目。‘牢’厂的音频指标需求，从 LHDC 的认证标准来看，是存在疑问的，而且‘牢’厂在需求包里明确提出是要过白金标：24bit/96kHz。在需求包上要求的音频指标 THD+N <= -90dB, SNR >= 110 dB, 与 LHDC 白金标的认证标准存在冲突，既然硬件都没向‘牢’厂反应这个问题，也就不多嘴了，免得招人烦。</br>

![llac_latency](https://i.loli.net/2020/09/01/H3RUrmnYKCzENbZ.png)</br>
_LATENCY_TEST_RESULT_ </br>
</br>
![lhdc_900](https://i.loli.net/2020/08/26/eUPrkIBNKFxJqVE.png)</br>
_LHDC_900_CERTIFICATION_STANDARD_

<!--
![lhdc_test](https://i.loli.net/2020/08/26/5dS2JOo4scnVGKX.png)</br>
_LHDC_TEST_ENVIRONMENT_
-->

因为‘牢’厂的音频指标参数和 LHDC 认证音频指标参数要求太高，查阅了能找到的蓝牙芯片规格书没有哪一家的蓝牙音频芯片能直接满足音频参数的要求。/br>

![qcc524_analog](https://i.loli.net/2020/08/28/DGfztPAulqHkyiZ.png)</br>
_QCC5124_SPECIFICATION_

![qcc5124_classAB_dac](https://i.loli.net/2020/08/28/xqZHn4GUimo5KBO.png)</br>
_QCC5124_CLASS-AB_DAC_ANALOG_OUTPU_
</br>

![be2300_dac_para](https://i.loli.net/2020/08/28/G2aRLr5doPnCZpO.png)</br>
_BES2300Y_PARAMETER_

BES2300Y 的音频指标参数从规格书来看，看起来是符合‘牢’厂的要求和 LHDC 认证要求，但给出来的参数 Fs 只有 48kHz, 96kHz 会怎么样心中没底，上 demo 板！单独测 LHDC 白金标音频指标没有问题，但输出功率不够；在通话模式下 LHDC SNR 左右声道只有72 / 73 dB，与普通蓝牙没有区别。音频指标参数更多的是硬件在看，但因为与软件的系统框架选择相关，在与‘牢’厂点对点特性摸底时的 HWA 评估报告因为只写了一句音频指标参数不达标被打回来要求重写。要满足音频指标参数的要求，看起来就只剩下一条路，走数字通道，加外置 DAC, 放弃蓝牙芯片自带的 DAC 。</br>

把 BES2300Y IIS 配置好编译后烧录到 demo 板上用示波器确认信号输出没错之后，在实验室里转了一圈没找到能用的 AP，都是测模拟信号的，问电声，电声说 IIS 没听说过，一脸郁闷，只好又去问硬件，硬件说 IIS 可以测试指标吗？肝痛！解释了一番之后，买测试设备的任务硬件就去找项目安排。过了差不多一周，采购设备的带上硬件和我去 ABTECH 看仪器，顺便把 IIS 的指标参数测了一下，116dB。HWA 基于 BES2300Y 方案的评估工作基本完成，可以开始写报告了。</br>

<!--
BES2300Y IIS 输出最大增益只能到 0dB, 规格书上标的digital gain: -70 -- 24 dB 是 "fake news"。国产芯片的规格书不靠谱是深有体会。</br>
-->

</details>

### BES2300Y
<details>
</br>
BES2300 是一颗功能集成非常成功的蓝牙芯片。 支持 ANC & ENC 并可支持第三方算法，支持 UAC 2.0 和 DSD 64/128， 支持 AAC / LHDC 等编码格式，支持 LBRT，支持 IIS 输出，支持双通道语音，支持 EQ，支持 GFP, 音频指标规格也定得很高，很强大的一颗芯片。</br>

但是，SDK 那就是一砣翔。第一次看 BES SDK 时，被它的按键代码给惊呆了，这么反人类的设计，是什么样的高人想出来的。任务调度也说不上有多严谨，只能说是在默认配置下功能能用。 对比 Qualcomm / Airoha 的 SDK 系统设计，BES 就是弟弟。曾尝试去改写一些功能模块， 遇到某个封装的 API 就改不动了，拿着民工的工资就不去操老板的心了。大家都是这样用，半斤八两，谁也不会比谁好到哪去。拿不到完整的 datasheet 去重构 BES 的系统框架这条路走不通。打开 IIS 功能后，硬件反应切换不了 USB audio，折腾了几天，发现在检测插入 USB audio 后软件启动了复位动作，这个复位动作在打开 IIS 功能后被使能，关掉复位，SDK 还会不会有其它隐藏的 bug 没法确定，还好在要求更新 SDK 后这种小 bug 基本没有再遇到了。</br>

SDK 基本正常了，赶紧把 EQ 调试功能打开，确认调试功能正常后整一台样机给电声调试，不能拖累小伙伴们的进度。没过几天电声反应写进软件的 EQ 曲线与调试时设定的 EQ 曲线不一致。又是什么鬼啊！？ 继续折腾 SDK， 艹， SDK 调用了一组默认的 EQ 把常用的 EQ 数组被屏蔽掉了，真是要骂娘了。赶紧修改更新给小伙伴。

<!--
BES2300Y 有两个版本4M flash版本和8M flash版本，PIN to PIN兼容。支持 ANC & ENC 并可支持第三方算法，支持 UAC 2.0 和 DSD 64/128， 支持 AAC / LHDC 等编码格式,      蓝牙耳机产品通常需要的功能：
-->

当我还在为蓝牙芯片到底是用 BES2300 还是 QCC5124 烦恼的时候，QCC5124 的 RF 性能和自带 DSP 功能以及音质这是我想要的，但对是否能申请到开放 DSP 并不确定，Qualcomm 代理商透露 Goertek 小伙伴选的方案是 QCC5124，我们也用 QCC5124 方案去做同一个客户同一项目原厂是否会支持这要画个问号。一月份‘牢’厂确定弃美方案，好了，这下只有 BES2300 可用了。听说 Goertek 的小伙伴因为这个原因春节只放了三天假，电子/软件重头来过，大家又在同一起跑线了，让你们跑得比我快，害我天天被‘牢’厂项目追。</br>

‘牢’厂的测试要求很多，测试标准通常会要求供应商应答满足与否, 不满足的要给出原因再来确认是否要修改。有次在与西安测试中心对标测试标准时，对测试标准上的蓝牙回连测试要求连续测试 10K 次成功率 100% 提出疑问。首先回连一万次成功率 100% 达不成这个目标，再一个即使某次连续测试能满足 100% 成功率但也不能保证这个结果可以复制。惊呆我的是西安测试中心工程师回答是即使在屏蔽房里测试只要能有一次能满足测试标准就可以，这个指标是给领导看的。我去！哪个被门夹的订的标准啊，真要按这个测试标准去测，还要写一套配套的测试软件，是不是存心恶心人。‘牢’厂有些指标让人无语，有些需求在产品量产前不得不砍掉 (放水)。老板挂在嘴边的舔语“我这些小伙子只会埋头做事，不会抬头看路”，你妹的，老子是乙方！</br>

AirPods 的多设备切换‘牢’厂也想搞，耳机只是接收端，取决于‘牢’厂的系统整合能力。

#### 蓝牙后台
</br>

![mode_switch_spec](https://i.loli.net/2020/09/01/BUQ5iJe31Sc2XGY.png)</br>
_有线无线切换要求_
</br>

蓝牙设备可以支持前/后台应用，检测到 usb 设备蓝牙保存状态信息应用挂起 (后台运行)，usb 设备移除，恢复状态信息，蓝牙回到前台，按照这个思路有线切无线应该可以满足快速切换的要求，但要解决不能让蓝牙事件唤醒蓝牙后台。无线切换有线，估计做不到快速切换的要求，设备枚举过程需要多少时间软件控制不了，取决于设备的兼容性。跟小满在电话里沟通一番后，对前后台的应用切换逻辑有疑问，只能再上海岸城。</br>

SDK 默认在蓝牙模式下插入 usb 是复位后再执行 usb device mount, mount 设备成功就切换到 usb 模式，不成功进入蓝牙模式，但是蓝牙没有后台模式，需要修改 SDK。芯片 RAM 是否能满足蓝牙前/后台切换应用，需要小满去确认。在一番讨论之后，这种做法可行，SDK 等小满更新，任务完成，打道回府，。</br>

#### 双通道语音
双通道语音一开始看到这个需求的时候并没有弄明白‘牢’厂要的是什么东西，后来才搞明白指的是音乐与提示语音同时播放。这个需求有没有用？想了想在通电话的时候还是有用的：耳机处在通话状态，如果电池电量低播报低电提示音如果没有双通道语音功能会切换到播提示语音再恢复通话，双通道语音能保证不会漏掉通话。把 BES SDK 翻一遍也没整明白这个功能要怎么搞，还是去海岸城搞起。在解释完需求后，BES 的工程师说功能是可以实现，就是提示语音要用不同的采样率去录制，占用 flash 存储空间，另外在不同的状态下播报提示语音时要去选择对应的语音文件，细节处理上会非常麻烦。又牵涉到 flash 空间，flash 容量的问题先放一边，后面系统设计的时候再去考虑。</br>
</br>
然后工程师又来一句，其实 LHDC 输出功率小我们也是可以有调整空间的，为了平衡功耗大小，所以输出功率设置没有开到最大。我日了狗了，之前在测试 IIS 的时候，我还特意与负责 IIS 的工程师确认过 IIS 输出最大是 0dB, 不可调。规格书上写的是 digital gain -70 -- 24 dB, 迷之答案，到底谁能给一个准确的回复。</br>
</br>
双通道语音功能可以实现，音量大小是否可以分别可设置，说是要确认，等回到办公室之后又他娘的没了下文，就算不能调节音量大小，好歹也吱一声啊。迷之 BES。</br>

#### OTA 与 双备份
OTA 功能蓝牙芯片都是具备的，但双备份还要支持回滚这个就很麻烦。按照‘牢’厂的需求存储结构划分为：</br>

    bootloader + app1 + app2 </br>

bootloader 中断向量映射到 app1 或 app2 物理地址并且随 app1/app2 乒乓切换 (从云端接收下来的应用程序不能固定存储在 app1 或 app2 位置)，来实现双备份并支持回滚。虽然 BES 的 OTA 功能的存储结构也是类似的设置，但 app2 是固定用来存储从云端接收的应用程序，而且在接收校验完成后要搬运 app2 的数据去覆盖 app1 的数据，就没办法实现回滚。双备份从字面上理解是新旧两份应用程序存储在本地，数据存储结构应划分为：</br>

    bootloader + app + app1 + app2 </br>

app 是当前在运行的应用程序， app1 和 app2 用来交替存储云端接收下来的应用程序，这种数据存储结构我认为才能称之为双备份。这种做法的好处是避开了中断向量映射这个麻烦问题，弊端就是占用大量的 flash 存储空间，而且跟 BES 的 OTA 功能类似需要搬运数据，在时效性上不如中断向量映射。</br>

‘牢’厂的十国语言提示语音需求已经占用了很大的 flash 存储空间，按英文提示音来评估，十国语言提示音就需要 2.2MB, 打开双通道语音功能提示音文件估计就占掉了 4.4MB, BES2300Y 内置的 4MB flash空间已经满足不了需求。BES2300 规格书上写支持 SPI 协议，能不能外挂 flash, 找 BES 寻求帮助。BES2300 还有 8MB flash 版本芯片，SPI 不支持 QSPI。在技术层面，还是想维持 SDK 本身的数据存储结构，即把提示音与应用程序打包在一起，如果单独划出一个区间用来存储提示语音文件，会不会带来其它问题不确定，但这样做 8Mb flash 也放不下提示语音文件。</br>

这种烧脑问题，待系统设计时再考虑。</br>
</details>


## System Design
<details> </br>

在春节前因为赶结构样板输出了第一版硬件，BES2300Y 控制触摸和佩戴检测。IQS572 是在生产组装前烧录 firmware, 但 IQS620 是在上电后写入初始化数据，默认的固件是以 60Hz 的频率给出 RDY 信号，在 RDY 为低 (持续 10ms) 的时候写入数据才有效。 单独配置中断触发 BES2300Y 检测 RDY 信号，可以正常触发 BES2300Y (用 GPIO 置反测试)，与 IIC 通讯结合在一起，就出现了异常，死活不能触发中断。在出样前一天晚上折腾了一个通宵，也没搞定，没招，死马当活马医，改成 50ms 定时扫瞄 RDY 信号，佩戴检测偶尔能用，也同样会引起触摸失效，没找到原因，只能先关掉佩戴检测输出样机。</br>
</br>
节后，第一版样机交付，但佩戴检测功能未实现。把 IQS620 规格书重新捋一遍，没捋出啥问题，佩戴检测异常还是没找到原因，触摸滑动功能也没整合好，在 demo 板上重新验证都正常，继续搬砖。坐下来搬个砖就各种哏。</br>

电声：烧个软件...</br>
电声：EQ 调试串口又连不上了...</br>
电声：ANC 芯片串口连不上了...</br>
硬件：升级一下软件...</br>
硬件: 串口工具用一下...</br>
测试：测试标准再捋捋...</br>
测试: 一起去松山湖对下标...</br>
项目: 这个需求是啥意思...</br>
项目: 这个时间结点写哪一天合适...</br>
项目: 什么时候可以出样啊...</br>
‘牢’厂: 微信上的问题出个报告...</br>
‘牢’厂: 今天的日报 5:00 要给我...</br>
‘牢’厂: 来下云谷讨论下工作安排...</br>
...</br>

每天小伙伴都要重复这些哏不让人消停。</br>

刚刚是要拿哪块砖？</br>
刚刚拿的砖放哪了？</br>
发呆ing准备干啥来的？</br>
艹，砖头放错地放了</br>
...

三月，‘牢’厂项目催软件 DRB 评审报告进度，只能先把系统框架先捋出来，要不然其他小伙伴进度也要被拖累，到时进度赶不上就是一大群人群殴我一个了。研究一番硬件小伙伴给过来的硬件框架图，啥东西画的框架图，歪歪扭扭，难以入目，强迫症复发，默默用 visio 重画再把软件需要修改的部分一并更新发回给小伙伴，让小伙伴在新版本上更新。</br>

评估摸底工作很多时候没有在‘牢’厂项目的时间进度节点完成，‘牢’厂项目都是按照 deadline 倒推安排进度，另一个他们也并不都具有技术背景，就没办法抓住评估工作中的技术难点去穷追猛打，真正把握住产品的开发方向，所以在遇到我认为重要的技术点时会花很多的时间去验证，但这种关键点通常不会主动告知‘牢’厂项目，一旦穷追猛打下去会多出很多无谓的报告，工作量会呈倍数的增加。跟‘牢’厂项目打交道还是要具备很强的承压能力。要求加人，老板安排一个小伙伴担当 SPM，对接‘牢’厂项目，很多会议我就不需要参与，项目计划这种烦心事就让小伙伴去面对，我就专心技术相关的工作。

十二月份的时候因为 usb 兼容性问题 BES 的回复不了了之，就准备外挂 usb audio codec 解决兼容性问题，再加上十国语言提示音一直没有很好的解决方案，就一直在准备外挂 MCU 来支持 SPI flash。因为对 ST 的 HAL 库和 LL 库还心有余悸，准备用 Microchip SAM L21，美芯不能用后，搞回 ST 准备用 STM32L431替代。 DRB 报告到底是用单芯片架构还是大-小核架构，看看 FreeLace 的 bug list，下不了决心，只能把‘牢’厂需求翻出来重新捋。</br>

![solution_cmp](https://i.loli.net/2020/08/26/ZFfS8lH2Y7gp3cP.png)
_BES2300 vs.BES2300+STM32L431_
</br>

‘牢’厂的第一代 Freebuds 应该是 Geotek 的小伙伴开发的，对 BES 方案体会应该是最深。听领导说 Geotek 与 BES 扯皮，BES 说 Geotek 开发能力不行，Geotek 说 BES 底层系统不稳定，到底怎么回事，看看 FreeLace 的 bug list, 萌新瑟瑟发抖！最重要的是对 BES 的技术支持没有信心，就象脚踩恨天高的美女看得到摸不着；找代理商很多时候还不如自己撸代码。</br>
</br>
继续整大-小核方框图，规划整体功能需求。</br>

![big_little](https://i.loli.net/2020/09/06/OvD9TZgVKtrJNfl.png) </br>
_NTG_BLOCK_DIAGRAM_ </br>

1. 有线升级 </br>
手机端通过 usb 总线通知 usb aduio codec 准备进入升级状态, usb audio codec 置 gpio 端口中断触发 mcu 将 usb bus swtich 切换到蓝牙端，手机与蓝牙通过 usb 总线握手成功后将升级数据包传给蓝牙，蓝牙再通过 uart 转发给 mcu, mcu 再通过 SPI 保存到本地 spi flash, 再由 mcu 制定升级策略。而且用 usb 总线可以兼顾‘牢’厂装备部门可维可测要求。</br>
2. OTA </br>
蓝牙收到数据通过 uart 转发给 mcu, mcu 再通过 SPI 保存到本地 spi flash，再由 mcu 制定升级策略， 蓝牙升级由 mcu 回传升级数据包。</br>
3. 触摸 & 佩戴：</br>
可能要一直维护到产品寿命终结，需要时间去优化用户体验。</br>
4. 蓝牙 </br>
需要增加蓝牙后台功能，修改升级相关的代码(蓝牙芯片仅负责收数据，是否升级由 mcu 来决定) 和增加 usb audio 模式下的降噪功能， SDK 蓝牙部分代码大体不需要修改，避免扛雷。</br>
5. 降噪 </br>
有线模式下还是要利用 BES2300 来支持通话降噪，音乐播放就切给外置的 usb audio codec, 功耗暂时兼顾不了。 </br>
6. 音频指标 </br>
播放音乐音频从 DAC 输出以满足音频指标要求，通话从 ANC 输出满足高清通话音频指标要求。 </br>

大-小核架构从方框图上看其它各功能模块软件也没有特别困难的地方，IIC / SPI / UART 都是常用的通讯协议。需要 BES 协助的都是底层相关，蓝牙应用层不涉及，也就不大可能需要担当背锅侠。五六家供应商竟争这一个项目，蓝牙芯片都是 BES2300，肯定会有供应商选择单芯片方案，如果友商单芯片方案走得通，再切回单芯片方案也不迟，硬件改动也不大。默默估算了一下开发时间，蓝牙基本上是交给 BES 修改，SDK 再整合一下一个月左右也差不多，触摸/佩戴/ANC/DAC/BMS/串口通讯搭出基本功能算二个月，升级功能估摸着要二到三个月，系统整合与优化也要二到三个月，全算下来七到八个月，现在才三月底，十一月量产，时间很充裕，顺利的话就算一杆枪也能准点打卡下个班。方框图看了又看，看看发际线好象又往上去了，需要生发核桃露补一补，咬咬牙还是选择大-小核架构推送给了小伙伴。第二版硬件走马登场，硬件和 BES 方案商商量后用蓝牙控制 mcu 的电源，蓝牙先启动， mcu 后启动，这个改动对软件功能实现影响不大。</br>

四月中完成 DRB 评审报告，项目开始投标，清闲了几周，等‘牢’厂的结果。项目问能不能中标？中标了有啥好处，真开始干活就不象评估摸底时那么懈意了。对所选择的系统框架还是有一定信心的，中标是八九不离十。四月底‘牢’厂释放了正式版 RFI，功能需求上仅拿掉了 DSD， 看过 RFI 后，对项目说， 中标， 稳了。按‘牢’厂的尿性，供应商至少两家，跟工程师打听没得到结果。中标了，听说报给‘牢’厂的 RFI 费用 700W+，大老板亲自跑过来搞了个誓师大会，那天被‘牢’厂工程师抓过去对标。鸡血打完，做事的还是这几个人。这个鸡血看起来是打给‘牢’厂了。 </br>
</br>
中标了，‘牢’厂就开始排资源需求，软件规划要 6 -- 8 个人，老板就把软件工程师的名字都挂上去，又把方案商的工程师也拉上，凑了 8 个人。不晓得又中了什么邪，又要加个 SPM。 “作死”的过程从此开始了。</br>
</br>
SPM 对项目的帮助实在有限。一个没有搬过砖的来规划搬砖的工作计划，怎么规划？产品需求都整不明白。也就只能当个传声筒，甲方的需求原封不动转达给工程师，工程师的意见再原封不动转达给甲方，这算是靠谱的。不靠谱的，把工程师的原话加上他自己的理解表达的可能是另一个意思。不幸的是 SPM 小伙伴就是这种不靠谱的，曾经的明言 “我是代表‘牢’厂来监督你们的”。这小伙伴忙没帮上尽添堵。一个产品开发结构、硬件、软件都需要有一个做整体规划的，这个做整体规划的他才清楚工作内容要如何拆分，每个结点的困难程度，进度要如何安排，人力资源要如何统筹，才有能力担当一个合格的 SPM，不是随便一个阿猫阿狗都能胜任。</br>
</br>
老板随后又来了个骚操作，软件开发工作全部交给方案商，搬砖的跟方案商的工程师学习，有领导附和佳和头戴耳机都是外发的不也做得很好，真想问下领导佳和是不是丢标了？俺也不敢问，俺也不敢说，举双手赞成，打个酱油它不香吗？方案商工程师上场，顶到了 SE 这个角色，赶紧移交资料，DRB 报告就再不用自己写了。FreeLace 也是这帮小伙伴开发的，就一面条耳机在 TR5 阶段的 bug list 还有多少项待完成的任务这帮领导心里难道没个 B 数吗？ </br>
</br>
好日子没过多久，又变卦了，方案商说他们人手不足，MMP 把 mcu 的开发工作又丢回来。看过方案商工程师移交的代码，不出所料 HAL 库，有功能，IIC 发送一个字节要 60ms 左右，再看不下去了，没有价值，用 LL 库重写代码。这时新来一小伙伴，就带着新来的小伙伴一起搞 mcu。</br>
</br>
忙到七月份，系统框架搭建完成，佩戴/触摸/BMS 这些功能都己经实现，正在考虑怎么把 flash 读写用 LL 库来实现和任务调度添加 free RTOS，‘牢’厂项目追 OTA 功能的进度，方案商的小伙伴邮件回复‘牢’厂项目蓝牙端的 OTA 功能二个月前已经完成了，mcu 端的升级功能一直未完成拖累软件的开发进度。在跟‘牢’厂、方案商小伙伴开会的时候我就不同意在 TR4 前去开发升级功能，基本功能需要用到 mcu 哪些资源都未完全确定去做升级功能可能会走很多弯路，浪费本就紧张的开发时间；技术层面操作 flash 需要关掉外部中断, 在不断添加功能的过程中就如果读写 flash 而漏掉关闭某个中断引起异常这种问题很难排查。在与方案商小伙伴开会讨论 uart 通讯协议时就醒小伙伴们用已知的 AT 指令、Ymodem、Zmodem 等协议作为参考来制订通讯协议，不要自己拍拍脑袋随便搞一套，误码率最好能设计为 0%, uart 通讯一定要先自己测试过再来联调。等收到方案商小伙伴的 uart 通讯协议一看，老娘的血压嗖的一下就上去了，立马无爱，一生黑。</br>
</br>
我们可能写不出高大上的代码，但是至少我们能把我们的代码写严谨，不要给自己或后来的小伙伴挖坑。小伙伴们看起来天天走得比我晚，在写代码的态度上不能让人认同。我们的 SPM 每天高呼老板说的都是对的，热烈拥护老板的英明决定，只管催进度这个功能明天能不能完成，而不管完成的质量。有天实在是看不下去了，对 SPM 说，最终我们所有人都是要对产品负责，如果产品做不出来，这些进度表没有任何意义。</br>
</br>
又是自己随便订了一套通讯命令，也没有握手命令，check sum 竟然是跟在指令之后，而不是放到一帧数据的结尾。一W个草泥马从胸中奔腾而过。新来的小伙伴说 OTA 以前做过，主动要求接下任务，对方案商的小伙伴失望之极，就把已经写好的代码推送给了小伙伴。</br>
</br>
新来的小伙伴在开发过程中，天天和方案商的小伙伴吵，争论 uart 协议命令如何制订，要不要加入重发机制，mcu 发送的数据有没有错， 蓝牙发送的数据有没有错 ... 我座位就在新来小伙伴旁边，本就被 LL 库改写 flash 读写操作搞得有点卡被这几个小伙伴吵得每天都是晕晕乎乎。跟新来的小伙伴讨论到底遇到了什么问题，小伙伴说 mcu 发送给蓝牙的命令方案商小伙伴说接收到的命令是错的，老是说 mcu 发送数据错误，uart 设置用的是我发给他的代码，都没有修改，连接 PC 端验证 mcu 发送的命令也是正确的。我跟新来小伙伴说，我们一起去找方案商小伙伴。一起讨论时，我跟方案商小伙伴说，不用怀疑 mcu 端的串口传输数据错误，串口 copy & compare 测试我跑了三天，没有发现数据错误。同样的蓝牙端的串口你也需要做同样的测试，接收数据错误可能是蓝牙端的串口有问题，如果解决不了找 BES 协助一下。 </br>
</br>
方案商的小伙伴测试时间稍微长一点就出现了数据错误，然后还解决不了，去原厂吧。出现问题的原因是小伙伴把 uart 通讯设在了蓝牙的应用层，串口通讯就在某些时候就一定会被打断，这时候接收/发送数据就出现了错误；SDK 默认的 uart buffer 只有 2K， 小伙伴开了 4K。这也是我不敢用单芯片架构的原因之一，BES 给出来的资料太少，你会不会踩中某个坑，不晓得。顺利趟过这个坑，才发现蓝牙端只写到了发送数据，发送完数据后要如何处理就没有了，方案商小伙伴在邮件里称之为已经完成了。如何将 mcu 的软件与蓝牙软件一起打包，如何拆分，之后又去找 BES 才完善。</br>
</br>
在双备份升级功能上与方案商小伙伴存在分岐，BES OTA 功能不能称为双备份，在 app2 替换 app1 的过程中如果关机后再开机 flash 只有 app2 一个备份，何来的双备份？‘牢’厂项目在之后也没有强调要双备份，做来做去还是回到了支持 OTA 升级这个需求。有线升级也存在分岐，原本的规划是支持 usb 升级, 方案商的小伙伴认为串口升级在 FreeLace 产品上已经经过‘牢’厂确认，用 usb 升级需要重新过‘牢’厂重新确认需要很多时间。我不确定这个小伙伴是如何说服‘牢’厂项目接受这个做法，usb audio 与 串口升级如何共存 (DP/DM用作串口)？ 可维可测重新烧录一套软件？这已经不是我认为最优的方案，没法满足‘牢’厂的需求。更别提之后将 ANC 和 DAC 的控制改回 BES2300Y 控制，切换 ANC 通过 IIC 写数据要占用多少时间会不会产生断音？会不会被蓝牙应用干扰？会不会产生 pop click？投标前在系统设计的时候因为这些问题存在风险，才选择了大-小核的系统框架，这下倒好把风险又给我带回来了。</br>
</br>
‘牢’厂的软件审核也就判断基本的语法是否符合规则，机器审核能看出来代码质量高低？不做白盒测试想要改善代码质量只能说是画饼充饥。‘牢’厂为什么会加不完的班，工程师在项目进度的逼迫下只能低质的完成交付，软件审核更多是流于形式，后来者在修复前面伙伴的低质交付时发现没法下手，面对一个十万级交付量的商业化产品谁敢轻易做决定软件重构，做好了是应该的，没做好以‘牢’厂的得性估计就是滚蛋了，绞尽脑汁可能发现只能又做个低质的修复，几次迭代下来，后面的维护工作就变得越来越棘手。有天在会议上老板问软件还需要多少时间来完成，邻导回句估计还要 400个工作小时。老板说那我给你们找 40 个人，10 天完成。我只能竖起大挴指说老板你牛B！如果大力能出奇迹，我们早就赶英超美走向火星了。</br>
<!--
我从不认为优秀的产品开发可以外包实现，外包一定是循迹最容易实现的路径，不会选择最优路径。对项目能否顺利完成我觉得是前路渺茫。有些老板潜意识觉得“总有刁民想害朕”，期盼外来的和尚好念经，你自己挖的坑只有自己埋。</br>
</br>
-->
在松山湖开 DRB 软件评审会议，‘牢’厂工程师也问不出个所以然，起不到查漏补缺的作用。审到串口通讯，也就问下波特率，发送机制，连是否带 DMA 都问不出来。DRB 上写的误差率为 0%，怎么实现的？BES 芯片外置晶振 26M，即使用 PLL 倍频，115200/128000 或其它波特率有哪一种在理论计算上能达到 0% 的误差率？串口通讯采用什么协议？通讯协议的纠错机制是什么？抗干扰性如何设计？通讯数据是否要加密？都是走过场。‘牢’厂工程师水的也不少就是了，也或许完全没有被实际设计系统毒打过。去松山湖一定要记得自备啤酒饮料矿泉水，瓜子花生八宝粥，一定要自备，一定要自备，一定要自备，重要的事情说三遍。从中午一点干到晚上十二点，害得胃痛都犯了。</br>
</br>
如何保证触摸准确率和触摸稳定性是在评估摸底时‘牢’厂项目提出来的问题，是开发过程中在技术层面我认为‘牢’厂提出的唯一一个有实际意义的问题。在投标前一直有在思考怎么回答这个问题，在我的系统框架下至少要涉及到四个层面：
1. 触摸芯片本身的触摸原理算法设计：是容性还是感性还是容感交互？汗渍或水珠对触摸特性的影响，算法设计时如何避免 </br>
2. mcu 与触摸芯片通讯机制与稳定性设计及系统响应机制 </br>
3. mcu 与 bt 通讯机制与稳定性设计及纠错机制 </br>
4. bt 系统响应机制与任务调度设计 </br>

‘牢’厂如果真要较真，这一个问题就够写一篇厚厚的论文，够我喝一壶都不止。可惜，之后‘牢’厂没人来较真。
</br>
有天闲聊时领导说友商已经投降了，开发进行不下去了，放弃了这个项目，‘牢’厂项目在问我们为什么要选择大-小核架构 (友商出来走两步？)。再一次证明了选择大于努力。
</br>
之后淡出了这个项目。
</br>
再之后，听说11月份‘牢’厂主动放弃了。‘牢’厂最后的选择还是要点个小红心:heart:。 </br>
<!--
有些老板对自己员工总是抱有“总有刁民想害朕”，期盼外来的和尚好念经。大多数时候你自己挖的坑只有自己埋。你给出一个你认为最优的方案，最大程度保证产品成功输出可能性在老板眼里可能就是一坨翔，非要去试下那个坑。‘牢’厂的 RFI 费用有那么好拿的？。‘牢’厂短距部门从一个 20--30 人的团队成长到 200--300 人的团队，还按照搞定某个人就一切太平的思路去做产品，做梦吧。产品开发过程中参与项目的就会换两三拔人，每个人都只会对自己的 KPI 负责，产品设计中的明显缺陷会放你过去，是他跟自己的 KPI 过不去？
-->

回顾这个项目从生到死，没有一个赢家。希望‘牢’厂不要再拿 FreeLace 这种产品收割消费者，还是回到那句话，合理搞钱，服务社会。</br>

</details>

## Code
<details>
@para L431RBIx_HSE_LPUART_DMA_printf.rar Description</br>
Re-routing of the C library printf function to the LPUART. The LPUART outputs a message on the HyperTerminal.</br>
  -- printf.c</br>
  -- printf.h</br>

The LPUART1 is configured as follows:</br>
-- baudrate = 115200 Baud </br>
-- word length  = 8 bits </br>
-- one stop bit </br>
-- none parity </br>
-- hardware flow control disabled </br>
-- reception and transmission are enabled in the time </br>

@para Dirctory *.c Contents </br>
-- L431RBIx_HSE_LPUART_DMA_printf\Src\adc.c </br>
-- L431RBIx_HSE_LPUART_DMA_printf\Src\cw2015.c </br>
-- L431RBIx_HSE_LPUART_DMA_printf\Src\gpio.c </br>
-- L431RBIx_HSE_LPUART_DMA_printf\Src\i2c.c </br>
-- L431RBIx_HSE_LPUART_DMA_printf\Src\iqs5xx.c </br>
-- L431RBIx_HSE_LPUART_DMA_printf\Src\iqs62x.c </br>
-- L431RBIx_HSE_LPUART_DMA_printf\Src\main.c </br>
-- L431RBIx_HSE_LPUART_DMA_printf\Src\printf.c </br>
-- L431RBIx_HSE_LPUART_DMA_printf\Src\pwrctl.c </br>
-- L431RBIx_HSE_LPUART_DMA_printf\Src\stm32l4xx_hal_msp.c </br>
-- L431RBIx_HSE_LPUART_DMA_printf\Src\stm32l4xx_it.c </br>
-- L431RBIx_HSE_LPUART_DMA_printf\Src\sy6970.c </br>
-- L431RBIx_HSE_LPUART_DMA_printf\Src\system_stm32l4xx.c </br>
-- L431RBIx_HSE_LPUART_DMA_printf\Src\usart.c </br>

@para Hardware and Software Environment </br>
-- This code runs on STM32L431xx devices.</br>
-- This code has been tested with STM32L431RBI6 and can be easily tailored to STM32L431CBT6 device.</br>
-- uVision version is v5.25.2.0

@para How to Use It</br>
In order to make the program work, you must do the following: </br>
-- open your keil uvision toolchain </br>
-- rebuild all files and load your image into target device </br>
-- run the code </br>
^_^
</details>

***

## Apple AirPods Max
在2020即将结束的时候，在12月8号 Apple 的头戴耳机 AirPods Max 发布。</br>
</br>
Apple Official Advertisement </br>
</br>
&nbsp;&nbsp;&nbsp; . High-fidelity audio </br>
&nbsp;&nbsp;&nbsp; . Active noise cancellation with transparency mode </br>
&nbsp;&nbsp;&nbsp; . Spatial audio for threater-like sound that sorrounds you </br>
&nbsp;&nbsp;&nbsp; . Stunning design with an exceptional fit </br>
</br>
Tech Specs </br>
</br>
&nbsp;&nbsp;&nbsp;Audio Technology&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;. apple-designed dynamic driver</br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;. acitve noise cancellation </br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;. transparency mode </br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;. acitve noise cancellation </br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;. adaptive EQ </br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;. spatial audio with dynamic head tracking </br>
</br>
&nbsp;&nbsp;&nbsp;Sensors&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;. optical sensor (each ear cup) </br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;. position sensor (each ear cup) </br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;. case-detect sensor (each ear cup) </br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;. accelerometer (each ear cup) </br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;. gyroscope (left ear cup) </br>
</br>
&nbsp;&nbsp;&nbsp;Microphones&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Nine microphones total: </br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;. eight microphones for active noise cancellation </br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;. three microphones for voice pickup (two shared with active noise cancellation and one</br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;additional microphone) </br>
</br>
&nbsp;&nbsp;&nbsp;Chip&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;apple H1 headphone chip (each ear cup) </br>
</br>
&nbsp;&nbsp;&nbsp;Controls&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;. digital crown </br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;. noise control button </br>
</br>
&nbsp;&nbsp;&nbsp;Weight&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;13.6 ounces (384.8 grams) </br>
</br>
&nbsp;&nbsp;&nbsp;Battery&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;. up to 20 hours of listening time on a single charge with active noise cancellation or</br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;transparency mode enabled </br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;. up to 20 hours of movie playback on a single charge with spatial audio on </br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;. up to 20 hours of talk time on a single charge </br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;. 5 minutes of charge time provides around 1.5 hours of listening time </br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;. storage in the smart case preserves battery charge in ultra-low-power state  </br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;. charging via lightning connector </br>
</br>
&nbsp;&nbsp;&nbsp;Connectivity&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;. bluetooth 5.0 </br>
</br>
