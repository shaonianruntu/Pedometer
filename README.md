# 智能运动记录仪

这是我使用 STM32F407芯片 和 MPU6050陀螺仪传感器 制作的一个电子计步器。

在 3.2 寸的 TFT 液晶屏上进行结果的显示。

测试显示其实现进度较为可观。

由于此次距离当时的制作时间已有一年多，所以资料不完整全完。部分后期的代码（添加 GPS 行程记录，GUI 美化）已经找不到了。

为了节省存储空间，我这里已经删除了编译所生成的临时文件，可以使用 keil5 重新编译生成。

## 项目研究意义
个人的身体健康在当下越来越受到人们的关注。智能运动记录仪可以记录步行或是骑行的里程、通过GPS记录位置甚至通过多机的通讯实现虚拟比赛等功能，大大增加了运动的可安排性与趣味性，是一款有利于身体健康的产品。

## 研究内容
本项目设计一个类似自行车码表的产品，除了LCD显示骑行速度、骑行里程外、日期时间外，增加了电池电量、电子指南针（当前方向）、转向及警示尾灯。如果时间充裕，再增加GPS行程记录（通过U盘保存）、GPS卫星状态、虚拟比赛（和之前行程记录做比赛对比（实时），通过I2S语音播报），后续也可以扩展从机模块，用于记录步行或跑步等等。

## 技术指标
1.使用STM32 MCU作为主控芯片

2.LCD界面显示

3.实现电子指南针功能

4.实现转向及警示尾灯的功能

5.实现电池电量监控

6.通过GPS实现行程记录

7.通过多机通讯实现虚拟比赛功能

## 关键问题
1.通过锂电池和升压、降压电路实现5V、3.3V两路电压输出

2.各芯片与元件的使用与代码的编写

3.若时间充裕还可实现多机通信、USB OTG功能、GPS功能并通过运行FREERTOS操作系统完成以上功能。

## 创新点
1.该记录仪将多种运动相关功能集中于一体

2.可以通过多机通信实现比赛等功能

## 项目实施方案
1.以STM32单片机作为主控芯片，实现USB、时钟、ADC等功能

2.使用开关电源芯片与3.7V锂电池提供5V与3.3V两路输出

3.使用nRF24l01模块、LCD模块等实现多机通信、LCD显示、电子指南针等功能
