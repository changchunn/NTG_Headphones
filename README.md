# NTG_Headphones

Apple的强大勿庸置疑，TWS耳机市场在AirPods出现前不温不火，AirPods出现后整个行业被引爆，“几番仍效法,至今仍领先”说的就是它。前段时间无意中看到一个新闻说是Apple要出一款高阶头戴式耳机AirPods Studio，不由得想起了两年前给‘牢’厂开发过的一款“胎死腹中”的高阶头戴式耳机。回顾这个项目“作死”的过程，反思过去工作中的是非得失，展望未来高阶产品开发成功之路。 </br>

(新闻链接：苹果头戴式耳机最新爆料 https://new.qq.com/rain/a/20200808A0JZIY00 )</br>

碰到错题还要划对勾的违心感。  
</br>
****
## 技术规格对比

![hwa_ntg](https://i.loli.net/2020/08/21/SdwEUAFBezZvaf7.png)</br>
</br>

![airpods_sudio](https://i.loli.net/2020/08/21/JtTcD145nOmVPZr.png)</br>

对比‘牢’厂和Apple的规格，相同之处都要求是High Quality Audio (‘牢’厂HWA), 支持ANC，支持Ear Detection, 这些技术规格用人话讲就是音质要好，信噪比要高，用户体验要佳(ANC让用户可以在嘈杂环境下使用，Ear Detect 即戴即使用，都可以归为用户体验)。</br>
蓝牙音频传输做死了SNR也不会超过75dB，High Quality Audio的SNR下限不会低于90dB，‘牢’厂就直接给出了SNR不低于110dB。

### AOV （Always-On Voice)
在应答阶段‘牢’厂在需求包之外会提出许多花样, 要求供应商应答他们再来评估是否要放到需求包中。语音控制就是其中之一, 涉及到两个方面：VOA与Voice Control。</br>
语音控制中文做的最好的就是科大讯飞，英文非Amazon莫属，我一个蓝牙音耳机要整得这么高大上吗？度娘
收到要求后，把知名的半导体和MEMS Microphone厂商官网挨个翻个遍，逐个去询信息，真被我逮到一家: OnSemi，奥力给！硬件也反馈Knowles IA610支持VOA功能。有了两家，可以应付‘牢’厂的需求了。 接下来就是一顿常规操作，约供应商介绍产品，讨论技术规格。</br>
供应链回复说OnSemi没用过所以没有联系方式，这个星球上经营理验别具一格的一家半导体供应商竞然不知道，吐血！回到OnSemi官网找到深圳Office的电话打过去，咨询负责的销售的联系方式，一听说是给‘牢’厂做产品，说‘牢’厂他们有专职销售并提供联系方式。拿到联系方式，反手打电话给‘牢’厂工程师，OnSemi销售你们比较熟，帮忙联系下要咨询Voice相关产品，同时发邮件给OnSemi‘牢’厂专职销售咨询工程窗口。就这样跟OnSemi勾搭上了。</br>
搭上‘牢’厂的虎威，找供应商要技术支持通常是一件较容易的事，这些业界牛B的供应商小厂去咨询要支持，那就是随便找个阿猫阿狗代理商(这已经是不错的待遇，再次一点的就是贸易商)来了解下有没有商机，很难拿到第一手信息，苦逼的只能把datasheet从头翻到尾，再从尾翻到头，或从某个不起眼的notes的字里行间找到你想要的数据。跟‘牢’厂配合这一方面还是比较爽的。</br>

#### Knowles IA610
Knowles MEMS microphone业界那是响当当。FAE介绍说 IA610 已经跟BES联调成功，申请参考代码，说是这个调试很麻烦云云, 不愿提供 (我勒个去，这哥们硬气，给不给参考代码是你的事，麻不麻烦那是我的事，哥 !)；申请demo平台，也提供不了，给建议去找 BES 申请。一听要找BES申请demo样机(BES是什么尿性？那基本都是有求无应)，赶紧寻求销售的帮助，无助于事。</br>
趁着别人还愿意打发你的时机，赶紧了解了一下 IA610 关注的相关特性。
IA610 是基于关键词的特征值语音识别算法，最多可以植入3段语音，如果是中文3段语音总共不能超过10个字(印象中是这个数据)，唤醒功耗 (识别到关键词唤醒并给出中断信号这整个过程) 大约电流3--4mA, 唤醒后提供一个中断信号给外部系统。</br>
了解了，告辞!

![ia610_current](https://i.loli.net/2020/08/22/oDtdxqERjwp5JU3.png)
_IA610_Figure1_

![ia610_int](https://i.loli.net/2020/08/22/DS9pzQyH8qRJen7.png)
_IA610_Figure2_

#### OnSemi
##### LC823450
LC823450是音频处理系统LSI，VOA功能仅是它所具备的功能中的一个模块，联系上海FAE在仅支持VOA功能的情况下给出的功耗曲线最低也在1mA左右。

![lc823450_current](https://i.loli.net/2020/08/22/eYWP6tUgqQdlLva.png)

##### Belasigna R281
支持Voice Wake-Up特性的MEMS Microphone; 另一家是OnSemi, 它有两款产品支持Voice Wake-Up, 分别是LC823450t和Belasigna R281。</br>


![r281_current](https://i.loli.net/2020/08/22/xlwNPJSbCjAkoet.png)
