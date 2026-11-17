# Nuphy Air96 V1

> 已卖，2023年4月29日 676 入手雏菊轴，2025年2月23日 350 转手

## 购买动机

1. 用 [K380](./logi-k380.md) 腱鞘炎
2. 96 和 75 价钱差不多，但是多一个小键盘

### 心路历程

排除了如下键盘：

#### [Magic Keyboard - US English - Apple](https://www.apple.com/shop/product/MK2A3LL/A/magic-keyboard-us-english) $99

国内市场为了做区分，直接把 Apple 2021 Keyboard (with ID) 划到了三代，三代就这样诞生了。但 [Magic Keyboard (Mac) - Wikipedia](<https://en.wikipedia.org/wiki/Magic_Keyboard_(Mac)>) 是没有 Generation 3 的概念的（笑；

海鲜市场的价格趋于稳定，据我所知，国航原装的价格直接低到了 300，当然这样的机会可遇不可求，所以我的预期一直都是 350，可惜捡不到，目前遇到最低欧版￥380（正常价）、国行￥420（不正常价、号有问题）；

所以暂时是捡不到了，PDD 百亿补贴活动的价格是￥580， 全新拆过的卖￥500；

因为卖的人不多，全是贩子，所以全都是死价，是没有办法砍的；

#### [NuPhy Air75 Wireless Mechanical Keyboard](https://nuphy.com/products/air75) $109.95（冷门）

又是一个冷门的产品，PDD 连个百亿补贴的活动都没得做；

淘宝更是没得看，在售的只有两家店：Nuphy 和 Nuphy 旗舰店，前者销量上吊打后者，但后者价格较前者便宜将近￥100；加上这款产品的分割商法（割掉的键帽还需要加价￥120），简直有点难以下手。

最想吐槽的是，后者的价格跳水真的很让人抓狂，甚至只是贵了￥10，我就已经不想买了。[NuPhy Air75价格历史查询](https://gwdang.com/trend/10063855043896-3.html)

矮轴听说手感稀烂，不如去买 FILCO(斐尔可)、NIZ(宁芝)，但是价格已经上千，已经超了两倍的预期；

唯一下得去手的、带 QMK 改键的，还是 的 K3P-H，但是 V2EX 上骂的又太多，

#### [Keychron K3 Pro QMK/VIA Wireless Custom Mechanical Keyboard](https://www.keychron.com/products/keychron-k3-pro-qmk-via-wireless-custom-mechanical-keyboard)


## 快捷键

- 侧灯：`FN + ? + ∧ / ∨ / < / >`
- F 键功能切换：` FN + X + F`
- 睡眠模式：`FN + X + C/V`
    - 闪绿灯 => 开启
    - 闪红灯 => 关闭
    - 下适用

## ISSUE: Nuphy Air95 Keyboard Function not works.

```shell
FN+X+F
```

via: [Nuphy Air75 - Function Lock](https://www.reddit.com/r/MechanicalKeyboards/comments/rlgy6c/nuphy_air75_function_lock/jw3d23q/)

另一个方案是：

```shell
echo 0 | sudo tee /sys/module/hid_apple/parameters/fnmode
```

via: https://www.hashbangcode.com/article/turning-or-fn-mode-ubuntu-linux

## References

1. 官方 https://nuphy.com/products/air96-wireless-mechanical-keyboard
2. 开源驱动 https://github.com/donn/nudelta
3. 说明书官方 https://nuphy.com/pages/user-manual
4. 说明书第三方 https://manuals.plus/zh-CN/nuphy/air96-wireless-mechanical-keyboard-manual
5. [求推荐一个真实使用的矮轴 - V2EX](https://www.v2ex.com/t/904227)
6. [有人用过 Keychron 不，吹的 Mac 最友好键盘 - V2EX](http://www.v2ex.com/t/826707)
