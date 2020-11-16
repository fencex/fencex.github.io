---
title : "阿里云 Composer 全量镜像php"
description : "阿里云 Composer 全量镜像"
tags :
  - "php"
date : "2020-11-02"
categories : 
  - "develop"
  -  "php"
menu : "main"
---


### 全局配置（推荐）

- 所有项目都会使用该镜像地址：
```
  composer config -g repo.packagist composer https://mirrors.aliyun.com/composer/
```
<!--more-->

- 取消配置：
```
  composer config -g --unset repos.packagist
```

### 项目配置

- 仅修改当前工程配置，仅当前工程可使用该镜像地址：
```
  composer config repo.packagist composer https://mirrors.aliyun.com/composer/
```
- 取消配置：
```
  composer config --unset repos.packagist
```
### 调试

请务必使用 -vvv 到底哪里卡住了，心中有数
- composer 命令增加 -vvv 可输出详细的信息，命令如下：
```
  composer -vvv require alibabacloud/sdk
```

### 遇到问题？

- \1. 建议先将Composer版本升级到最新：
```
  composer self-update
```
- \2. 执行诊断命令：
```
  composer diagnose
```
- \3. 清除缓存：
```
  composer clear
```
- \4. 若项目之前已通过其他源安装，则需要更新 composer.lock 文件，执行命令：
```
  composer update --lock
```
\5. 重试一次，若还有问题，请到钉钉群：23178217 反映。