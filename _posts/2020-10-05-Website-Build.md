---
layout: post
title: Ubuntu+Apache搭建
---

Date: 10-05 2020 15:07 Monday


#### Ubuntu安装 ####
1. 前往Ubuntu官网下载对应镜像（18.04）
2. 在虚拟机中或电脑中安装ISO镜像文件
3. 在完成安装之后设置root账号名与密码
4. 修改Ubuntu的镜像源为清华镜像源：
    + ```
      # 备份源地址
      sudo cp /etc/apt/sources.list /etc/apt/sources.list_backup 
      ```
    + ```
      # 修改源地址文件中的源为清华源
      sudo vi /etc/apt/sources.list
      ```
    + ```
      # 将sources.list中的内容替换为:
      
        # 默认注释了源码镜像以提高 apt update 速度，如有需要可自行取消注释
        deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic main restricted universe multiverse
        # deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic main restricted universe multiverse
        deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-updates main restricted universe multiverse
        # deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-updates main restricted universe multiverse
        deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-backports main restricted universe multiverse
        # deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-backports main restricted universe multiverse
        deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-security main restricted universe multiverse
        # deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-security main restricted universe multiverse

        # 预发布软件源，不建议启用
        # deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-proposed main restricted universe multiverse
        # deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-proposed main restricted universe multiverse
      ```
      >Ubuntu清华源使用帮助：https://mirror.tuna.tsinghua.edu.cn/help/ubuntu/>
