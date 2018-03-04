---
ID: 406
post_title: GH4视频拍摄的最佳设置
post_name: gh4-setup-for-filmmaking
author: banpie
post_date: 2018-03-04 21:39:28
layout: post
link: >
  http://wp.bpteach.com/gh4-setup-for-filmmaking/
published: true
tags:
  - 影视
categories:
  - 传播
---
GH4 最新的固件2.4中已经加入了Vlog的配置，这一款强大的无反视频机设置繁多，这篇文章主要介绍如何修改机器的一些默认设置，以最大化的方便视频的拍摄。

## 1. 获取全部设置功能
将拍摄模式调节至`Creative Video Mode `

## 2. 切换至手动对焦模式
旋转相机背侧的对焦模式至`MF`

## 3. 切换至单张拍摄模式
 旋转相机顶部左侧的旋钮至`单张拍摄`
 
## 4. 复位至出厂设置
进入`Setup`菜单中，在第五页中选择`Reset`
## 5. 设置地区与时间
复位成功后，按照提示设置地区与时间

## 6. 设置Setup菜单
1. `Beep`: 
	- `Beep Volume`: `OFF` 
	- `E-Shutter Vol`: `OFF`
2. `Headphone Volume`: `6`
3. `Monitor Luminance`: `1`
4. `Menu Information`: `ON`（打开菜单详细信息提示）
5. `System Frequency`: `24.00Hz CINEMA`
6. `Live View Mode`: `30fps`

## 7. 设置Motion Picture菜单
1. `Photo Style`: 2.4固件下推荐`V-log`,2.2固件下推荐参见下文的*设置Picture Style*
- `Rec Format`: `MOV`
- `Record Quality`: 24帧拍摄推荐`4K/100M/24P`；高帧拍摄推荐`FHD 100M 24P`，该模式下可开启`VFR`可变帧率，最高可设置96帧Slowmotion拍摄
- `Exposure Mode`:  `M`（如果拍摄为25P，快门速度不能低于1/25）
- `Continuous AF`: `OFF`
- `Metering Mode`: `Center Weighted`(选项2)
- `Luminance Level`: `0-255 `
- `Sound Output`: `REC SOUND`
- `Mic Level Disp`: `ON`（此后的设置需要关闭`Variable Frame Rate`才可设置）
- `Mic Level Adj.`: `-12db`
- `Mic Level Limiter`: `OFF`
- `Wind Cut`: `OFF`

## 8. 设置Custom菜单
1. `Eye Sensor AF`: `OFF`
- `AF Assist Lamp`: `OFF`
- `Direct Focus Area`: `ON`
- `AF+MF`: `ON`（该设置使得在自动对焦的模式下，半按快门时仍然可以调节手动对焦环进行对焦）
- `MF Assist`: `AF Mode Button` (选项3, 直接通过物理Fn按钮放大所选区域)
- `Peaking`: `ON`
	- `Set`
		- `Detect level`: `Low`
		- `Display Color`: `Orange`
7. `Histogram`: `ON`
8. `Zebra Pattern`: `ZEBRA2`（超出100%的过曝区域）
	- `Set`
		- `Zebra 1`: 70%，适用于让人脸获得正确曝光
		- `Zebra 2`: 100%，适于于显示高光过曝的区域
9. `Guide Line`: `九宫格`
10. `Constant Preview`: `ON` 
11. `Exposure Meter`: `OFF`
11. `Video-Priority Display`: `ON`（调节拍摄显示的参数为视频模式，比如帧率，码率，bite rate等）
11. `Dial Set`
	- `Assign Dial`: `SS/F` (用顶部旋钮调节快门速度，用背部旋钮调节光圈大小）
	- `Exposure Compensation`: `Rear Dial`
11. `Eye Sensor`
	- `Sensitivity`: `Low`
	- `LVF/Monitor Switch`: `Mon` 
11. `Touch Settings`/`Touch AF`: `OFF`
11. `Shoot W/O Lens`: `ON`

## 9. 设置Picture Style
下面设置的模式不仅可以保证画面的质量，同时也后期提供了较为灵活的空间

1. 进入`Motion Picture`菜单
2. 在`Photo Style`中选择`Natural`选项
3. 修改参数如下：	
	- `Contrast`: -3
	- `Sharpness`: -5
	- `Noise Reduction`: -2
	- `Saturation`: 0
	- `Hue`: +2

## 10. 设置手动白平衡
**在拍摄的过程中，绝对不要使用自动白平衡!**自动白平衡的设置会使得素材根据光线条件自动调节白平衡参数，会给后期的调色带来许多不便之处。

- `AWB`: 不要使用
- `Daylight`: 自然光，适用于户外拍摄
- `Cloudy`: 适用于户外多云天气的拍摄
- `Shade`: 适用于户外阴暗天气的拍摄
- `Incandescent`: 钨丝灯
- `Custom White Balance (1-4)`: 可以利用18%的灰度卡保存多达4项的自定义白平衡设置
- `Manual White Balance`: 手动设置色温值