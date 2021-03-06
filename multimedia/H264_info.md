---
title: H.264相关
date: 2017-12-25 16:12:33
category: multimedia
---

H.264，又称为MPEG-4第10部分，高级视频编码是一种面向块，基于运动补偿的视频编码标准。
到2014年，它已经成为高精度视频录制、压缩和发布的最常用格式之一。

## H.264码流中SPS PPS
SPS Sequence Paramater Set，又称作序列参数集。
PPS Picture Paramater Set，图像参数集。

在H.264的SPS中，第一个字节表示`profile_idc`,根据`profile_idc`的值可以确定码流符合哪一种档次。

```java
    private static final byte[] SPS = {(byte) 0x00, (byte) 0x00, (byte) 0x01, (byte) 0x67, (byte) 0x4d, (byte) 0x00, (byte) 0x1f, (byte) 0xe5, (byte) 0x40, (byte) 0x28, (byte) 0x02, (byte) 0xd8, (byte) 0x80};
    private static final byte[] PPS = {(byte) 0x00, (byte) 0x00, (byte) 0x01, (byte) 0x68, (byte) 0xee, (byte) 0x31, (byte) 0x12};
```

## 参考
* [H.264码流中SPS PPS详解 - DaveBobo](https://zhuanlan.zhihu.com/p/27896239)
* [H.264先进的视频编译码标准 - CSDN](http://blog.csdn.net/gl1987807/article/details/11945357)
* [RGB、YUV和YCbCr](http://blog.sina.com.cn/s/blog_a85e142101010h8n.html)
