---
title: sftp上传文件夹
tags: Linux, 学习
categories: Linux
comments: true
date: 2018-02-19 21:25:09
---
使用hexo写博客,完成后将生成好的静态文件上传到服务器上。
利用sftp将本地文件夹E:\yixuan2016.github.io\public（包含子文件夹）,复制到服务器/usr/share/nginx/html/blog/目录下

> 命令: put
> 环境：win10
> 命令行工具：cmder

步骤:
1. sftp登录到服务器
   `λ sftp root@twogether.cn`
2. 首先定位到远程/usr/share/nginx/html/blog/目录下：    `cd /usr/share/nginx/html/blog/`
3. 本地定位到E:\yixuan2016.github.io\public目录下：     `lcd E:\yixuan2016.github.io\public`
4. 执行命令：    `put -r ./*`
5. 命令执行完成 本地文件便全部复制到远程文件夹中。
