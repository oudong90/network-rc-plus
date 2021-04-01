# Network RC -  Remote Control Car Software For Raspberry Pi

[中文](./README-cn.md)

Network RC' feature:

- low-latency control and network video￼ ￼transmission
- 27 custom channels(PWM or Height/Low)
- touch, gamepad, keyboard, RC transmitter
- real-time listening and voice sending
- repoviding NAT traverse
- voice broadcast
- playing audio
- remote shared

## 依赖

- ffmpeg: 运行前请确保树莓派上安装了 ffmpeg，安装方法 `sudo apt install ffmpeg -y`
- nodejs

> **注意：在最新树莓派系统上存在兼通性问题， 使用此版本系统<http://downloads.raspberrypi.org/raspbian/images/raspbian-2020-02-07/>**

## 安装

```bash
bash <(curl -sL https://network-rc.esonwong.com/download/install.sh)
```

## 使用教程

- 改装 RC 遥控车
  - 视频教程: [4G 网络 RC 遥控车 02 - DIY 网络控制改造教程](https://www.bilibili.com/video/BV1iK4y1r7mD)
  - 图文教程: [WiFi 网络遥控车制作教程](https://blog.esonwong.com/WiFi-4G-5G-%E7%BD%91%E7%BB%9C%E9%81%A5%E6%8E%A7%E8%BD%A6%E5%88%B6%E4%BD%9C%E6%95%99%E7%A8%8B/)
- 4G 远程控制
  - 视频教程：[4G 5G 网络 RC 遥控车 03 - 无限距离远程遥控？](https://www.bilibili.com/video/BV1Xp4y1X7fa)
  - 图文教程：[网络遥控车互联网控制教程](https://blog.esonwong.com/%E7%BD%91%E7%BB%9C%E9%81%A5%E6%8E%A7%E8%BD%A6%E4%BA%92%E8%81%94%E7%BD%91%E6%8E%A7%E5%88%B6%E6%95%99%E7%A8%8B/)

## 代码贡献指引

```bash
git clone https://github.com/itiwll/network-rc.git
cd network-rc/front-end
yarn # or npm install
yarn build # or npm run build
cd ..
yarn # or npm install
sudo node index.js
```

打开 `http://[你的树莓派 ip 地址]:8080`

## 使用

```bash
# 基本使用
node index.js

# 设置密码
node index.js -p password

# 启用网络穿透
node index.js -f -o 9088 --tsl

# 自定义网络穿透服务器
node index.js -f -o 9088 --frpServer xxxxxxxxxx --frpServerPort xxx --frpServerToken xxxxx
```

## 接线图

![GPIO](./gpio.jpg)

## 树莓派软件下载

- [network-rc.esonwong.com](https://network-rc.esonwong.com/download)
- [github](https://github.com/itiwll/network-rc/releases)

## 社群

### 微信群

交流请移步微信群，入群方法添加微信 `EsonWong_` 备注 `Network RC`

## 捐赠

![微信赞赏吗](https://blog.esonwong.com/asset/wechat-donate.jpg)

## 链接

- [作者 B 站主页](https://space.bilibili.com/96740361)
- [爱发电支持 Network RC](https://afdian.net/@esonwong)

## Credits

- [ws-avc-player](https://github.com/matijagaspar/ws-avc-player)
- [@clusterws/cws](https://github.com/ClusterWS/cWS)
- [rpio](https://github.com/jperkin/node-rpio)
- [rpio-pwm](https://github.com/xinkaiwang/rpio-pwm)
- [xf-tts-socket](https://github.com/jimuyouyou/xf-tts-socket)
- Eson Wong - 提供免费的 frp 服务器
