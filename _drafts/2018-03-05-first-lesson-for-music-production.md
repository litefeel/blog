---
ID: 453
post_title: 音乐制作的第一门课
post_name: first-lesson-for-music-production
author: banpie
post_date: 2018-03-05 11:24:52
layout: post
link: http://wp.bpteach.com/?p=453
published: false
tags:
  - Mooc
  - 传播学理论
  - 笔记
categories:
  - 音乐
---
# L1:声音和信号流

## 1.1 声音的传播：Propagation

- 声音可以通过空气、铁、水等介质进行传播
- 空气中的湿度、温度、海拔等等都可以影响声音的传播
- 一般而言，我们讲声音的速度主要是用340m/s来衡量，也就是1km/3s，
- 声音的delay，reverb，phasers还有flangers，这些都和声音传播这个概念有关，比如你要模拟一个room的环境感，你就要计算声音通过墙壁反射回来声波的时间（Sound‘s location within a space）。

## 1.2 声音的振幅
- 对应的音量
- 声音在吉他上的传播与声音的传播方向是垂直的，它是呈现波形的状态，上下波动向前的；声音在空气中得传播是与传播的方向平行的，直线向前的；这两点可以通过一个弹簧来呈现，它上下摆动会发出声音，前后也会；摆动的幅度也大，声音就越大；
- 在声音的波形表中，我们不用平行的方式来表示，是因为那个太难呈现了，所以我们用波形来表现音量
- 空气中的音量的大小我们用DBSPL来表示，也就是decibels of sound pressure level，这个系统是和我们人耳可以听见的0db为界限的；
- 电脑的音量则是用DBFS，也就是decibels of full scale这时候0db则是最大的界限，剩下的都是负的；
- 动态范围Dynamic range指的是The amplitude range in decibels between the noise floor and distortion

## 1.3 声音的频率
- 对应的音调
- 声音振动的越快，音调越高；反之则越低
- tibre is the collection of sound in multiple frequencies，或者说是harmony 和声
- sine wave: energy at a single frequency
- EQ可以作为控制声音频率的工具，比如boost the bottom end，也就是调高低频率声音的音量
- 人耳能够听见的声音频率范围：20hertz-2k hertz；1 hertz = 1/s
- 儿童可能会听到高频的声音，但是长大后这部分的听力组件消失；女人的听力范围可能偏高；人耳本身就是一个eq，我们在某个范围的听力会比较敏感；

## 1.4 声音的可视化
- Oscilloscope最常见的波谱:横坐标是时间，中坐标是振幅；
- Spectrum Analyzer波谱:横坐标是频率，纵坐标是振幅；
- Spectrogram: like the spectrum analyzer repeat over time
- 可以在三个图谱中看一个sine wave 和Octave higher的变化: double the frequency

## 1.5 设备的连接
从Analog到Digital：
- 声源：物体或人
- 声音：引起空气的震动
- 麦克风：麦克风讲空气震动的模拟转换为电流的变化，也就是analog信号
- XLR：麦克风输出线缆，形成Low level audio signal
- Audio Interface：Mic preamp；line level audio signal；analog to digital converter（2进制的信息）
- USB/火线：连接电脑设备
- DAW：电脑的软件
- USB/火线：连接输出设备

从Digital到analog则是相反的过程

## 1.6 麦克风：输入转换器
- 麦克风的原理

## 1.7 麦克风的分类
- condenser：一般用于录音室；非常的灵敏；收音的范围很广；需要48v的电源；推荐第一个麦克风购买Condenser；
- dynamic：适合舞台；外表坚固；只收取附近的声音

## 1.8 麦克风的频率反应
- 查看麦克风的频率波谱
- AKG C414基本就是收取所有的声音
- Shure SM58就是收取人声比较多，低频高频都被调低了

## 1.9 麦克风的指向性
- 心型
- 锐心型
- 超心型、
- 双向（8字型）
- 无指向（全向型）：会反应出声音所处的位置

## 1.10 麦克风的放置
- 把品牌logo放置在摄像机前面就对了

## 1.11 line level and gain staging 
- plus 4 ：业界领域标准
- minus 10：消费领域标准
- [两个标准的区别](http://www.motu.com/techsupport/technotes/document.1998-10-14.7006918204)

## 1.12 Cable
- 很多问题的出现都是线缆出现了问题，重新插拔一下可能就好了
- ts cable：quater inch cable，一般是instrument cable
- trs cable：一般连接耳机
- xlr cable：一般用于麦克风，减噪效果好
- direct box：把ts input转换为xlr input
- 3.5mm cable：一般用于耳机
- rca cable：红白黄线缆，一般用于消费级别的设别

## 1.13 数字音频接口
## 1.14 麦克风连接和增益
- 连接麦克风之前，把level ctrol还有扬声器关闭
- 增益应该从低的开始，慢慢增加

## 1.15 Anolog to Ditigal信号转换

## 1.16 pick up connection
## 1.17 DAW数字音频工作站

# L2
## 2.1 Analog to Digital Conversion
- bits，也就是dynamic range
- sampling rates 每隔多少时间采样一次，我们采样的频率越高，可以收集的对应的声音频段就越准确：比如采样频率为40000hertz，那么可以采集到2000hertz的声音
- 应该设置为
- cd的bit是16 bit，44100khz，因为这个频率是人的耳朵在
- 如果在daw中，播放的时候把4000herz的声音调节成8000herz播放，音调会增高

## 2.2 buffer size
- buffer size越小，delay的现象就越不明显
- 当我们在录制声音的时候，buffer size调低至128 samples左右
- 当我们在剪辑的时候，调节到1024
- 如果我们使用48khz的采样率，buffer size设置为128 samples，那么我们获得的delay在2 milliseconds

## 2.3 file type
- 音频的压缩的概念：mp3是压缩格式，所以在我们录制的时候，最好使用wav（最好是broadcast wav因为有保留原数据）或者aaff无损格式
- 推荐24bit，48000hertz，并确保interleaved files（保留左右声道）

## 2.4 project folder
- 一般项目文件会包含许多的文件夹，比如元数据，项目文件，声音源文件等等
## 2.5 proproduction checklist
1. proper project name and location
2. digital audio preferences：sample rates（48000 hertz）
3. file type（broadcast wav）
4. hardware settings（设置input和output）
5. buffer size （128 为基础）

##  2.6 multitrack
- audio track
- midi track
- auxiliary track：一个中介的track，一般是一个submix
- instrument track：读取midi设备的乐谱，然后输出通过频率合成器合成的音乐
- global track：marker，temple，key change等等都在这里操作

## 2.7 录制音频 checklist
- check setting（设置level：调低gain，插入乐器，打开phantom power）
- 创建input的track的时候，记得选择mono track
- name the track 
- record enable the track
- set the level using the microphone preamp 
- enable the click and coutoff
## 2.19 midi
- music instrumental digial audio
- midi channels range from 1-16
- 常见的midi message：note on 或者off；control change；pitch bend
- 还有2个data word分别是音高还有弹奏的力度，这两个数据用7bit来表示，也就是 a range of 0-127
- “panic”：means turn all notes off
- “sustain” is control channel 64
- “channel pressure” is also known as “after touch” 
- “synthesizer”create sound from a geometric wavafrom or  formula
- “sampler”plays back pre-recorded audio



## 3.4 效果分类
- dynamic effect：和amplitude有关，通常是控制音量，包括：compresors，limiters，expanders，noise gates
- delay effect：用于表现声音的空间感，包括：reverbs，delays，phasers，flangers，choruses
- filter effect：high pass filter，low pass filter，band pass filter，parametric eq，graphic eq 

## 3.5 insert
- dynamic还有filter通常在insert中设置
- delay的effect通常在aux track设置，帮助节省cpu空间
- 常用的技巧包括：
		- adding insert
		- bypassing insert
		- choose preset
		- saving preset
		- changing order of isnerts
		- copy/paste inserts