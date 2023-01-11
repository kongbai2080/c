# 用STM32制作一个简易停车场自动计时计费装置
基础：
1. 模式一：当单片机串口接收到"ON"指令后，打开门(用舵机代替），此时开始计时。       
          当收到"OFF"指令后关门。停止计时，结束此次计费。
2.模式二：用超声波控制开门，当距离小于某个值(自己设定)时开门，再次经过时关门。
3.模式三：使用摄像头控制开门，摄像头识别一个方形的靶子(颜色任意)将摄像头图像显示在屏幕上(屏幕种类不限)，并且能将目标的大小显示到屏幕上，当屏幕上的目标大小大于某个值（自己设定）时开门。                                 
拓展:
1.使用STM32的内置ADC，读取舵机信号线输出波形。以舵机转动（开门）时作为开始，记录保存往后5s内的波形数据，在屏幕上显示该波形的FFT变换图形
2.自行设计至少两级菜单的UI并使用

注：要实时显示计费时间和停车费。为了测评方便，计费按每5秒5元计算（未满5秒按5元收费)。
   串口接收可以选择蓝牙等无线接收装置，也可以用usb转ttl通过上位机（串口调试助手）与电脑通信
   允许和自己老大交流思路
