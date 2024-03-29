# escpos 指令打印机驱动

*仅仅自己研究测试使用，精简而不全；因为自己也是遇到问题才更新！*   

---

😀 TSPL指令集的打印机请跳转[https://github.com/lilindog/TSPL-Printer](https://github.com/lilindog/TSPL-Printer)

---


💡 最近我看到有博客引用该库，我接下来准备重构一下:     
1. 改善代码结构（分层），增加escpos指令的打印状态获取; 最近在研究tsc打印指令；等我缓过来就来完成这些工作。     
2. 图片转bitmap算法自己实现（目前正在做）,去除之前的node环境的相关依赖，更方便于移植到如小程序、混合app的蓝牙打印场景。       
*为了实现上面第2个需求，最近花了很多时间去掌握lz77、huffman、crc以及png、jpg等图片的二进制结构。*   

---

## 介绍
适用于nodejs的小票打印机驱动。  
已在mac端、pc端、树莓派端(nodejs、nwjs) 下跑通。  

## 应用场景
nwjs/electron 驱动小票打印机打印菜单小票。   
nodejs 驱动打印机打印菜单小票。   

## 使用
直接看examples中的示例代码。  
或者看源码。  

## 注意
目前只针对佳博[(佳博官网)](http://cn.gainscha.com/default.php)80mm系列印机和广州优库打印模组[(模组官网简介)](http://www.chinayoko.com/index.php?m=Product&a=show&id=251)使用usb连接方式做了测试，确保能正常使用。
其它牌子的打印机没有做实测，不过理论上来说只要打印机支持escpos指令即可兼容，也有可能各家打印机在指令兼容上面各有微调。   
网络打印目前没有搞， 哪有鸡巴时间来搞。

## 测试效果
* [使用该库辅助实现的一个简单的硬件收银机](https://www.bilibili.com/video/BV1AB4y1K7cW/)      
* [80mm打印机测试视频](https://www.bilibili.com/video/BV1Xo4y1d7pf/)     
* [58mm打印模组测试视频](https://www.bilibili.com/video/BV1uN411d7KU/)   
