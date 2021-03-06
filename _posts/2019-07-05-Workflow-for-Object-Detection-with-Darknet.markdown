---
layout: post
title:  "使用Darknet进行Object Detection的工作流程"
date:   2019-07-05 12:59:35 +0800
categories: [solution]
tags: [object-detection]
---
`样本标注`[labelImg] -> `模型训练`[darknet] -> `模型部署`[darknet-serving] -> `效果展示`[gouchicao-video]

## 样本标注 [labelImg]
```bash
# [PRE-DEFINED CLASS FILE]和[SAVE DIRECTORY]先创建好，再执行。
$ python3 labelImg.py [IMAGE PATH] [PRE-DEFINED CLASS FILE] [SAVE DIRECTORY]
```
* 支持`pascal voc`格式和`yolo`格式

> 狗吃草提供了`pascal voc`格式到`yolo`格式的转换工具[voc2yolo.py]

![labelImg 标注安全帽](/assets/images/labelimg-helmet.jpg)

## 模型训练 [darknet]
* 提供容器化的工具[darknet image]
* 提供创建模型训练工程的命令[create_project.py]
* 提供生成部署模型数据的命令[generate_model_deploy_data.py]

## 模型部署 [darknet-serving]
* 提供容器化的工具[darknet-serving image]
* 一键部署模型

## 效果展示 [gouchicao-video]
* 支持图片、图片目录
* 支持视频文件
* 支持实时视频

![gouchicao video 绘制目标检测对象](/assets/images/gouchicao-video-helmet.jpg)

[labelImg]: https://github.com/gouchicao/labelImg
[darknet]: https://github.com/gouchicao/darknet
[darknet-serving]: https://github.com/gouchicao/darknet-serving
[gouchicao-video]: https://github.com/gouchicao/gouchicao-video
[voc2yolo.py]: https://github.com/gouchicao/darknet/blob/master/voc2yolo.py
[darknet image]: https://cloud.docker.com/u/gouchicao/repository/docker/gouchicao/darknet
[darknet-serving image]: https://cloud.docker.com/u/gouchicao/repository/docker/gouchicao/darknet-serving
[create_project.py]: https://github.com/gouchicao/darknet/blob/master/create_project.py
[generate_model_deploy_data.py]: https://github.com/gouchicao/darknet/blob/master/generate_model_deploy_data.py

## 参考资料
* [labelImg](https://github.com/gouchicao/labelImg)
* [darknet](https://github.com/gouchicao/darknet)
* [darknet-serving](https://github.com/gouchicao/darknet-serving)
* [gouchicao-video](https://github.com/gouchicao/gouchicao-video)
* [模型动物园](https://github.com/gouchicao/darknet/tree/master/model-zoo)
