---
layout: post
title:  "图像识别整体解决方案"
date:   2019-07-08 06:59:35 +0800
categories: 图像识别
---
`样本标注`[labelImg] -> `模型训练`[darknet] -> `模型部署`[darknet-serving] -> `效果展示`[gouchicao-video]

## 样本标注 [labelImg]
* 支持`pascal voc`和`yolo`格式
* 使用过程要注意的是，通过命令行指定的输出目录要提前创建

![](https://raw.githubusercontent.com/tzutalin/labelImg/master/demo/demo3.jpg)

> 狗吃草提供了`pascal voc`到`yolo`格式的转换工具[voc2yolo]

## 模型训练 [darknet]
* 提供容器化的工具[darknet image]
* 整理出工程目录结构

## 模型部署 [darknet-serving]
* 提供容器化的工具[darknet-serving image]

## 效果展示 [gouchicao-video]
* 支持展示图片、图片目录、视频文件、实时视频
![](https://github.com/gouchicao/gouchicao-video/raw/master/predict/image-helmet.jpg)

[labelImg]: https://github.com/gouchicao/labelImg
[darknet]: https://github.com/gouchicao/darknet
[darknet-serving]: https://github.com/gouchicao/darknet-serving
[gouchicao-video]: https://github.com/gouchicao/gouchicao-video
[voc2yolo]: https://github.com/gouchicao/darknet/blob/master/voc2yolo.py
[darknet image]: https://cloud.docker.com/u/gouchicao/repository/docker/gouchicao/darknet
[darknet-serving image]: https://cloud.docker.com/u/gouchicao/repository/docker/gouchicao/darknet-serving
