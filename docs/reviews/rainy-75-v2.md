# Rainy 75 V2 Review / 雨 75V2 评价

## 优点

1. 做工扎实，铝坨坨分量足，1.5kg；
2. 声音好听，大键一致性好；

## 缺点

Windows 下几乎没有缺点；

Mac 下全是问题：

1. 无法改 F区 功能键：F区为固件保留，无法修改 [^fn-change]
2. CapsLock
  1. 没适配 Mac 输入法切换，切换后大小写触发；
  2. 大小写指示灯亮灭延迟；
3. 蓝牙指示灯未适配 Mac：连接 Mac 后（MacOS 27.0.1），蓝牙指示灯，不断闪戳，昏暗环境下很刺眼；

[^fn-change]: 短期内目测也不能改, 一代就无法修改，算是 ”祖传设计“

专门拍了一个视频压力官方，不过大概率没用：

https://www.bilibili.com/video/BV19Gs56oEgv/

### 曲线救国

问题 1, 2.1 都可以通过 hammerspoon 写脚本勉强用，这是我的脚本配置：

https://github.com/bgzolab/hammerspoon-config

唯独问题 2.2, 3 是它固件的问题，我一点办法都没有
