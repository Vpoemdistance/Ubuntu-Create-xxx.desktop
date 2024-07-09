# 帮助在Ubuntu（Desktop）上创建桌面快捷方式 .desktop文件
## 简介
当我们在Ubuntu（Desktop）上使用一个应用程序时，总是希望能够方便快捷地启动它，这时候我们希望能够如Windows一般能够在桌面创建一个快捷方式，但Ubuntu上很多软件不一定自带快捷方式，本文记录本人的实践过程，希望有所帮助。

When we use an application on Ubuntu(Desktop),we always hope to be able to start it quickly and easily.At this time,we hope to be able to create a shortcut on the desktop like Windows,but many software on Ubuntu do not necessarily come with shoorcuts.This article records my practice process and hopes it will be helpful!

##  第一步
在目录： /usr/share/applications 下创建chrome.desktop

打开文件夹-其他位置-计算机-usr-share-applications

```
cd /usr/share/applications
sudo vim chrome.desktop
```
## 第二步
在chrome.desktop中输入以下内容：

```
[Desktop Entry]
Name=Chrome
Comment=MYCHROME
Exec=/home/username/doc/chrome/extract/opt/google/chrome/chrome
Type=Application
Terminal=false
Icon=/home/username/doc/chrome/extract/opt/google/chrome/product_logo_256.png
```
Name：图标显示的名称
Exec ：启动程序路径
Icon：图标路径

## 第三步
复制chrome.desktop到桌面，并给权限

```
sudo cp chrome.desktop ~/Desktop

sudo chmod +x ~/Desktop/chrome.desktop
```

## 第四步
双击，即可运行

如果不行，则右键图标，点击允许执行
