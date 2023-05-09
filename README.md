# r329语音识别模块配合mqtt
---
## 效果说明
r329的语音识别模块会在识别到有人喊 “**救命**” 后发布警告到mqtt服务器，然后被其他远程设备的订阅端订阅。
## 运行过程
- 进入工程目录
  `cd Maix-Speech-mqtt`
- 启动语音识别模块
  `sudo ./maix_asr asr_wav.cfg`
- 启动订阅端（可将Maix-Speech-mqtt/mqtt/mqtt_sub.py复制到其他远程设备运行，python中需要安装paho-mqtt包）
  `./mqtt/mqtt_sub.py`
- 喊救命后远程设备的订阅端能够收到警报

详情见：https://github.com/sipeed/Maix-Speech/blob/master/usage_zh.md
