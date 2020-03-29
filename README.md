
# OCP2PCIe-AltiumDesigner

本分支基于 [OCP2PCIe-AltiumDesigner A1.1Beta](https://github.com/xiaoxinpro/OCP2PCIe-AltiumDesigner/tree/A1.x
) 项目升级而来，在原来的基础上增加了5V电源转换电路（理论将支持全部OCP主板），增加了5V与12V电源供电的风扇插座（为4CM风扇提供电源将有更好的散热）。

> 如果你是小白，无需安装任何软件，直接从 *打样* 章节开始看即可，其他内容可无视。

## 原理图

OCP转PCIe电路与前一版本完全相同

电源电路使用LM2576-5V将12V降压到5V，可以最大提供3A的电流，将为OCP 5V与风扇5V提供电力，为后续DIY提供5V电源支持。同时还将支持跳线12V与5V直连，为低成本方案提供可行性。

风扇驱动电路采用5V插座和12V插座两种选择，可自由选择5V或12V的4CM风扇，多余的风扇接口也可以为其他需要风扇的设备提供风扇电源。风扇电源提供限流电阻RF1和RF2，可强制为风扇限速，降低噪音，若不需要限速可以焊接0欧姆电阻或导线直连。

![OCP2PCIe-AltiumDesigner 原理图](https://upload-images.jianshu.io/upload_images/1568014-739a80ba074a98bc.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

## PCB

本分支PCB外形原项目保持一致，OCP转PCIe电路 layout 没有修改，将原空闲电路增加了电源电路与风扇驱动电路。

![OCP2PCIe-H-F-4 A2.0Beta](https://upload-images.jianshu.io/upload_images/1568014-5955e791869871ab.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

## 打样

本分支使用 Altium Designer 19 绘制，因此可直接将项目的 `OCP2PCIe-H-F-4.PcbDoc` 文件发送给打样厂家，例如：嘉立创。

打样参数如下：（仅供参考）

|名称|参数|
|---|---|
|板子层数|2|
|板子尺寸|10.00cm x 8.28cm|
|板子厚度|1.6mm|
|阻焊覆盖|过孔盖油|
|焊盘喷镀|*沉金* > *无铅喷锡* > *有铅喷锡*|
|铜厚|1盎司|

> 关于焊盘喷镀，建议使用 *沉金* ，可以长时间保护金手指防止氧化导致接触不良，性能与其他方式基本无差别，但价格较高。

## 采购元件与焊接

可根据原 [OCP2PCIe](https://github.com/xiaoxinpro/OCP2PCIe-AltiumDesigner/blob/KiCad-V1/doc/UserGuide_zh.md) 项目说明进行元器件购买和焊接。

元器件清单如下：

* BTB 120pin 0.8mm 插座
* 0805 0R 电阻 （可选）
* 待更新。。。

大插座有防呆设计，反装是装不上的，直接把所有脚焊上即可。

板子背面的 `TP1` 位置焊接一个0R电阻，如果没有可直接用一坨锡代替。

> 更多内容与详细内容请查看原 [OCP2PCIe](https://github.com/KCORES/OCP2PCIe/) 项目相关说明。

## 参考

* [Altium Designer](https://www.altium.com.cn/)
* [OCP2PCIe](https://github.com/KCORES/OCP2PCIe/)
