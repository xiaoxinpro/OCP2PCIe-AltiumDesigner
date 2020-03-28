
# OCP2PCIe-AltiumDesigner

本分支基于原 [OCP2PCIe](https://github.com/KCORES/OCP2PCIe/) 项目使用 Altium Designer 19 重新绘制的转接板。

> 如果你是小白，无需完整任何软件，直接从 *打样* 章节开始看即可，其他内容可无视。

![OCP2PCIe-H-F-4 A1.1Beta](https://upload-images.jianshu.io/upload_images/1568014-7e8113da97d984a7.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

## 原理图

本分支原理图与原项目 KiCad 的原理图完全相同，这里不再赘述。

## PCB

本分支PCB外形、元器件封装、元器件位置与原项目保持一致，PCB layout 重新优化绘制。

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

可根据原 [OCP2PCIe](https://github.com/KCORES/OCP2PCIe/) 项目说明进行元器件购买和焊接。

元器件清单如下：

* BTB 120pin 0.8mm 插座
* 0805 0R 电阻 （可选）

大插座有防呆设计，反装是装不上的，直接把所有脚焊上即可。

板子背面的 `TP1` 位置焊接一个0R电阻，如果没有可直接用一坨锡代替。

> 更多内容与详细内容请查看原 [OCP2PCIe](https://github.com/KCORES/OCP2PCIe/) 项目相关说明。

