# spl（视频流）
内部视频传输到公网上

## 一、架构说明


## 二、公网上的架构
公网上采用EasyDarwin开源包，作为接受拉推流服务器。
具体操作方法：https://github.com/EasyDarwin/EasyDarwin
操作系统：centOS

## 三、内网上的架构
内网上采用FFmpeg工具进行推流，具体部署在“消防智能计算中心”上
推流方法如下：ffmpeg -i  "rtsp://admin:qinchao098@192.168.3.116:554/cam/realmonitor?channel=2&subtype=1" -rtsp_transport udp -vcodec h264 -f rtsp rtsp://localhost/3
X86版本
Arm版本：

## 四、内外网通信
在外网服务器上搭建消息队列服务器，“消防智能计算中心”实时对需要推流的数据进行监测
