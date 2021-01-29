
binwalk在玩杂项时是个不可缺的工具。
1.最简单的，在玩隐写时，首先可以用它来找到其中的字符串
例如：
在铁人三项，东北赛区个人赛中，有一道题
它直接给了一个文件，没有后缀，不知道是什么文件
先binwalk下，命令就是直接binwalk 文件名。返回了一个字符串信息，发现  pohsotohp，是Photoshop的倒写。将文件用Python脚本倒写后，用图片工具打开发现flag。找字符串的信息也可以用stegsolve

2.判断类，一个图片中藏有一个压缩包，或者有其他图片，或者这就是一个压缩包，改了后缀而已

例如：binwalk一张图片后发现里边有另一张图片的信息，可以用dd工具或者winhex根据位置将另一个文件提取出来

3.解压类，binwalk后发现是Linux的文件系统或者是固件的文件，
binwalk -eM，直接将文件解压出来。

4.binwalk里面就有分离文件的功能。binwalk -D=jpeg oddpic.jpg 这样就可以，-D=类型就会分离出那种类型的文件到一个文件夹里

# Binwalk

[![Build Status](https://travis-ci.org/ReFirmLabs/binwalk.svg?branch=master)](https://travis-ci.org/ReFirmLabs/binwalk)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://GitHub.com/ReFirmLabs/binwalk/graphs/commit-activity)
[![GitHub license](https://img.shields.io/github/license/ReFirmLabs/binwalk.svg)](https://github.com/ReFirmLabs/binwalk/blob/master/LICENSE)
[![GitHub stars](https://img.shields.io/github/stars/badges/shields.svg?style=social&label=Stars)](https://github.com/ReFirmLabs/binwalk/stargazers)

Binwalk is a fast, easy to use tool for analyzing, reverse engineering, and extracting firmware images.

### Installation and Usage

* [Installation](./INSTALL.md)
* [API](./API.md)
* [Supported Platforms](https://github.com/ReFirmLabs/binwalk/wiki/Supported-Platforms)
* [Getting Started](https://github.com/ReFirmLabs/binwalk/wiki/Quick-Start-Guide)
* [Binwalk Command Line Usage](https://github.com/ReFirmLabs/binwalk/wiki/Usage)
* [Binwalk IDA Plugin Usage](https://github.com/ReFirmLabs/binwalk/wiki/Creating-Custom-Plugins)

More information on [Wiki](https://github.com/ReFirmLabs/binwalk/wiki)

# Binwalk Professional Edition

After years of developing and supporting binwalk as an open source project we have finally sold out to the man and released a cloud-based firmware extraction engine called *Binwalk Pro*. After all someone needs to pay devttys0 so he can buy more milling equipment and feed his children (in that order). Please consider subscribing and reap the benefits of getting actual customer support for all your firmware extraction needs. Please visit https://www.refirmlabs.com/binwalk-pro/ for more information. 
