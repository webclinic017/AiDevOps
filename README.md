devEops 😆 Develop a self-operation and maintenance platform

Travis Build Status Github All Releases MIT licensed 😋

Author: YoLoveLife.com 👌

Operation and maintenance system solution (growing)
💪 Practice an operation and maintenance platform centered on assets and application information
django & rest-framework & bootstrap
💪 Referenced many Django projects. My Django is really great
travis & Django TestCase
💪 Unit testing. The test is not standardized but I try to do it

If you are interested in: automated operation and maintenance, operation and maintenance resource management, etc. ⭐ me, share it with other operation and maintenance personnel
If you are interested in: Django development, rest-framework, etc. ⭐ me, share it with other developers
Please ⭐ me!!! Please ⭐ me!!! Please ⭐ me!!!

Regarding the problems I encountered in development, I will write them in the issues for friends in need 🔍 Query
These questions are the conclusions I reached after searching a lot of information and trying a lot of solutions 😬
You can search for helper in issues to view the related questions I wrote. I wrote them very carefully.
If you don’t find the question you are concerned about or you have suggestions for my project, please discuss with me in issues ❤️ Looking forward to receiving your information
Contents

Introduction
Platform Overview
How to Install
Automatic Operation and Maintenance Function Implementation

Introduction

This self-operation and maintenance platform is committed to the integration and automated operation and maintenance of IT resource information, and provides assistance for operation and maintenance through the integration of service and application configuration information.
devEops is growing

All operation and maintenance operations are based on the correctness and consistency of information integration (asset information management) 💾
📊 Provide statistics on asset information, the proportion of application systems, the number of scripts/playbooks called, etc.
Temporary collection of application information (such as MySQL status, etc.)
All operation and maintenance operations (scripts | plays) will automatically inject asset information when submitted and be remotely executed through ansible
All asset information and architecture information are stored in the database for all operation and maintenance personnel to operate
Developers can log in to the platform to submit work orders to initiate firewall modifications, application releases, daily operation and maintenance 🕘 and other operations, and operation and maintenance personnel can allow operations to proceed
All application releases and daily operation and maintenance work schedules are displayed 📅
Detailed permission operation, distinguishing between developers and operation and maintenance personnel

Platform Overview
Login Interface

LOGIN
Host Management

HOST
Batch Host Information Upload

UPLOAD
Script Writing

SCRIPT
Timeline Display

TIMELINE
How to Install

devEops depends on python2.7, many python third-party modules and mysql database
The following operating environment already has python2.7 and mysql database

$ cd path/to/project/folder/

#Install python third-party library
$ pip install -r requirements.txt

#Connect to local database and create data table structure
$ vim apps/deveops/settings.py #Enter database connection method in DATABASES
$ python apps/manage.py makemigrations
$ python apps/manage.py migrate

#Start service
$ python apps/manage.py runserver &
#Start by default at port 8000 You may need an nginx as a Web server

Self-operation and maintenance function implementation

devEops :laughing: 开发自运维平台
================================
[![Travis Build Status](https://travis-ci.org/YoLoveLife/DevOps.svg?branch=master)](https://travis-ci.org/YoLoveLife/devEops)
[![Github All Releases](https://img.shields.io/github/downloads/atom/atom/total.svg)](https://github.com/YoLoveLife/devEops/releases)
[![MIT licensed](https://img.shields.io/badge/license-MIT-blue.svg)](./LICENSE.md) :yum: </br>

Author: [YoLoveLife.com](http://www.yolovelife.com) :ok_hand: </br>

运维体系解决方案(正在成长中)</br>
:muscle: 实践以资产、应用信息为中心的运维平台</br>
django & rest-framework & bootstrap</br>
:muscle: 参考了诸多django项目 我的Django用的真的很棒</br>
travis & django TestCase</br>
:muscle: 单元测试 测试不规范但是努力去做

如果你关注：自动化运维、运维资源管理等内容  :star: 我,[分享](http://www.yolovelife.com)给其他的运维人员</br>
如果你关注：django开发、rest-framework等内容  :star: 我,[分享](http://www.yolovelife.com)给其他的开发者</br>
求求你们 :star: 我吧!!!   求求你们 :star: 我吧!!!   求求你们 :star: 我吧!!!</br>

*关于我开发中遇到的问题 我会写在issues当中供有需要的朋友 :mag: 查询*</br>
*这些问题都是在查询了诸多资料并亲身尝试大量解决方案 :grimacing: 最后得出的结论*</br>
*您可以在issues中搜索**helper**查看我写的相关问题 我写的很用心*</br>
*如果未找到您关注的问题或者您对我的项目有建议请在issues和我讨论 :heart: 期待收到您的信息*</br>

## Contents
* [介绍](#introduce)
* [平台一览](#looklike)
* [如何安装](#howtoinstall)
* [自运维功能实现](#whatcando)
## <a name="introduce"> 介绍 </a>
本开发自运维平台致力于IT资源信息的整合与自动化运维，通过服务、应用配置的信息整合来运维提供帮助。</br>
devEops正在不断成长
- 所有运维操作都基于信息整合的正确性和一致性(资产信息管理) :floppy_disk: </br>
- :bar_chart: 提供资产信息的统计,应用系统的占比、脚本|剧本的调用次数等</br>
- 可临时搜集应用上的信息(如MySQL的status等信息)</br>
- 所有运维操作(脚本 | 剧本)在提交的时候会自动注入资产信息并通过ansible远程执行</br>
- 所有资产信息、架构信息都存储在数据库中供所有运维人员操作</br>
- ~~开发人员可登陆平台提交工单发起防火墙修改、应用发布、日常运维 :clock9: 等操作,运维人员许可操作进行~~</br>
- ~~所有应用发布、日常运维工作日程展示 :date:~~ </br>
- 详细权限操作，区分开发人员以及运维人员 </br>

## <a name="looklike"> 平台一览 </a>
### 登陆界面
![LOGIN](img/login.png)</br>
### 主机管理
![HOST](img/host.png)</br>
### 批量主机信息上传
![UPLOAD](img/upload.png)</br>
### 脚本编写
![SCRIPT](img/script.png)</br>
### 时间线展示
![TIMELINE](img/timeline.png)</br>

## <a name="howtoinstall"> 如何安装 </a>
devEops依赖于python2.7、诸多python第三方模块以及mysql数据库</br>
以下操作环境已经拥有python2.7以及mysql数据库
```bash
$ cd path/to/project/folder/

#安装python第三方库
$ pip install -r requirements.txt

#连接本地数据库并创建数据表结构
$ vim apps/deveops/settings.py #DATABASES中输入数据库连接方法
$ python apps/manage.py makemigrations
$ python apps/manage.py migrate

#启动服务
$ python apps/manage.py runserver &
#默认启动在8000端口 你可能需要一个nginx做Web服务器
```
## <a name="whatcando"> 自运维功能实现 </a>
