# Keyboards

Everything about my keyboard

## About me

键盘触发原理大致分为：静电容、霍尔、磁力、机械、薄膜，目前我只用过后两个;

偏好：

1. 可维护性，矮轴可玩市场真是太差了；
2. 压力系数一定要 30-40 之间，超过 40g 的谨慎购买，压力太大了
3. 铝坨坨很好，但不能放在笔记本电脑上用，尤其是 Mac，塑料不是全是缺点；
4. 适配 Mac 布局 + 快捷键，最好直接放上去就可以用；
5. 固件开源，特别是 ZMK/QMK

## Overview

以下是对品牌的一些偏见和看法

### Keychron

> [!WARNING]
> CTMD 不送防尘罩

> 最早是从 AK 的频道听说这个牌子

他们家主打一个中高端的品类，公司在香港，国内外都有耕耘，优点有不少：

1. Mac 适配，都听说过 K3Max 吧，算是比较出圈的爆款了；
2. 操作规范，因为面向国际化，使用 QMK/VIA 比较合规，开源的键盘也比较多，主要有：
    1. [qmk_firmware](https://github.com/Keychron/qmk_firmware): QMK 官方固件的 Keychron 分支，包含了 Q、V、K Max 等 63 款以上键盘的源代码、构建配置和键位映射
    2. [zmk](https://github.com/Keychron/zmk/tree/rtl8762g)：ZMK 开源固件的分支，主要针对部分追求无线续航的新款型号（如“Ultra 8K”系列）。

官网是 https://keychron.cn，产品线其实很复杂，部分之间其实没有什么明显的区别，多注意甄别部分键盘是否开源。

以上是软件方面，而我最不喜欢的就是他们家的轴体，太单调了，而且似乎不愿意做低压力系数的轴，最低压力的线性轴都是 40~45g 的红轴，对我这个肌无力患者很不友好。

## Nuphy

> [!WARNING]
> CTMD，从 AirV3 开始不送防尘罩了，就为了强推自己家卖 200 的皮套

> 最早是想要一个通勤的键盘，选择了矮轴，经过 V友 推荐入手 Air96[^personal-talk]

矮轴起家，最早也是做 Mac 生态起来的，也是主打中高端，最近一两年逐渐下探，主打的一个宣传场景就是把键盘放在 Mac 上使用[^personal-talk]，从最早的 NuType F1 到 Nuphy Air75，一下子公司就爆了[^save-nuphy]

[^personal-talk]:虽然我当时不懂，直接买的是Air96配列，完全避开了这个绝美的使用场景。

[^save-nuphy]: https://www.gcores.com/articles/181393

自我接触 Nuphy 以后，他们迭代了三代，算是比较快，比较卷的了吧？

一代算爆款，不多评价，除了软件难用一点之外，没有什么大的毛病；

二代算是正统续作，在一代基础上，放弃了那个巨难用的驱动，开始使用 QMK+VIA，开源了QMK固件[^nuphy-open-source]，也推出了更多的轴体，算是我最满意的一代；

[^nuphy-open-source]: https://github.com/nuphy-src/qmk_firmware/tree/nuphy-keyboards/keyboards/nuphy

而到了最近一代，就比较有看头了，我专门[骂过他](docs/reviews/nuphy-air75-v3.md)，从类Top结构+金属定位板，变成 Gasket + PC 定位板[^layout-change-nuphy75v3]，加了底棉填充，手感和声音是上去了，但是呢？根本拆不开，毫无维修价值和客制化，万一电池鼓包[^battery-swelling]了怎么办？

[^layout-change-nuphy75v3]: https://www.bilibili.com/video/BV11Q8jz2Ew1/
[^battery-swelling]: https://www.ptt.cc/bbs/Key_Mou_Pad/M.1735094325.A.3D4.html

轴体呢？他们这一代彻底把轴体推倒重来，导致之前所有的轴体都不可用了，更难受的是，截止我写这段文字的时候，芦荟轴已经停产了，只剩二手市场的个人商家在卖了，你怎么看？24 年发布的键盘，不到两年时间，芦荟轴就销声匿迹了，矮轴变成了快销品。

![](https://pub-89c11651a8434f18a530bd6f93e399da.r2.dev/2026/20261116224932356.webp)

而且，前 5 年积攒的所有 Gateron 生态，继续推倒重来：

- Nuphy Air60 V1/V2
- Nuphy Air75 V1/V2
- Nuphy Air96 V1/V2
- Keychron k7
- Keychron k7 Pro
- Keychron k7 Max
- Keychron k3
- Keychron k3 Pro
- Keychron k3 Max
- Keychron k15 Max
- EPOMAKER LUMA84
- James Donkey(贱驴) S1 

有好处吗？当然，他们终于开始做标准化了，最大的体现就是 Kick75 支持高矮轴切换，确实采用了5针设计，这与标准高轴的针脚布局是一致的，NuPhy 官方也明确宣传：

> nano 轴使用MX轴脚设计，可兼容高轴轴座
> https://m.weibo.cn/status/5158601282815982

![](https://pub-89c11651a8434f18a530bd6f93e399da.r2.dev/2026/20261116225106062.webp)

虽然 Air75V3 高轴插不进去，但起码整体真的奔着高轴去做了，它的“脚”已经和高轴统一了。

明年大概就会迭代新的产品了吧，真希望Nuphy能够把三代砍掉的东西加回来，不过大概率也不可能了，CTMD:

1. 防尘罩；
2. 增补轴；
3. 老婆贴纸；

## Shame Wall

### 不标配防尘罩

> 买之前记得先看下开箱视频，然后再确定要不要买，没有防尘罩绝对是大忌！

没有防尘罩的[^fcz_source]：

1. feker
2. NuPhy（2026后续系列）
3. 八位堂
4. 怒喵
5. 燃风
6. crush80
7. evo80
8. 小蜜蜂奇点80
9. ikbc108
10. rog夜魔
11. 罗技
12. 维咖
13. 雷蛇
14. 洛斐
15. 车厘子
16. ck
17. cherry
18. 柯芝（部分无）
19. atk（部分无）

对应的，送防尘罩的：

1. 宁芝
2. hi75c（仅成品，套件无）
3. 迈从
4. ainbell
5. 狼蛛
6. 前行者
7. akko
8. rk
9. 黑爵
10. 猫尔本
11. coolkiller
12. 雨75
13. evo75
14. 惠普
15. vgn（京东无）
16. 黑峡谷
17. ikbc87
18. 新盟
19. 阿米洛
20. 极光80
21. 达尔优
22. 凌豹
23. 魔咖
24. epomaker
25. colorreco
26. 腹灵
27. ilovbee
28. OMO100

[^fcz_source]: https://xhslink.cn/o/6qDgtNh3nDl

## Tools

1. VIA 改建: https://usevia.app
2. 在线测试: https://www.zfrontier.com/lab/keyboardTester/

## Community

1. V2EX - 键盘 https://www.v2ex.com/go/mechanical
2. QMK 耻辱棒 https://docs.qmk.fm/license_violations#offending-vendors
