ESP32-S3-DevKitC-1
基于ESP32-S3主控的蓝牙语音控制移动机器人项目

📖 项目介绍
本项目采用ESP32-S3-DevKitC-1开发板为主控，通过蓝牙串口与手机通信，支持语音指令控制舵机运动，实现机器人前进、后退、左右转向等动作。
开发环境：Arduino IDE，天问Block。
通信方式：HC-04蓝牙串口通信，天问语音模块ASRPRO核心板。
执行部件：360°连续旋转舵机，OLED显示屏。

✨ 主要功能
1. 蓝牙无线连接手机APP控制。
2. 语音指令解析，控制机器人运动姿态。
3. PWM精准控制舵机转速。
4. 串口打印运行状态信息。

🛠️ 硬件清单
主控开发板：ESP32-S3-DevKitC-1 。
蓝牙模块：HC-04 。
语音模块：天问语音模块ASRPRO核心板 。
执行舵机：SG90 360°连续旋转舵机 * 4。
电源：5V稳压电源 。

📝 引脚接线说明
ESP32-S3引脚定义：
GPIO2  接右后侧舵机。
GPIO3  接右前侧舵机。
GPIO5 接OLED显示屏I2C_SDA。
GPIO6 接OLED显示屏I2C_SCL。
GPIO13  接左前侧舵机。
GPIO14  接左后侧舵机。
GPIO15 接HC-04 RX。
GPIO16 接HC-04 TX。
GPIO17 接天问语音模块ASRPRO核心板PA6。
GPIO18 接天问语音模块ASRPRO核心板PA5。

天问语音模块ASRPRO核心板引脚定义：
MIC+,MIC-接麦克风。
SPK+,SPK-接扬声器。
PA6 接ESP32-S3的GPIO17。
PA5 接ESP32-S3的GPIO18。

🚀 使用方法
1. 将代码上传至ESP32-S3开发板。
2. 直接用提前设置的语音命令控制。
3. 微信小程序搜索“蓝牙串口_江协科技”搜索配对HC-04模块。
4. 打开串口调试APP，发送指令控制机器人动作。

📂 仓库文件说明
ESP32_Bluetooth_Voice_Robot_Servo/：项目完整源代码Arduino工程文件。
test_SERV：360°舵机零点校准工具。
Voice.txt：语音文件 。

💡注意：
ESP32_Bluetooth_Voice_Robot_Servo中使用了Arduino中的库函数，使用时需先下载。
PCB图中的“语音下载”需使用ASR-LINK自动下载器下载。
舵机运动时的噪音很大，会影响麦克风的准确率。
