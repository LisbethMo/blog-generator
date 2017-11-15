---
title: 用Hexo搭建博客系统
date: 2017-11-16 03:49:58
tags:
---
稍微简述一下搭建博客系统的步骤：

  1、初始化

    - 首先在我的 GitHub 上新建了一个空的repo，项目名字叫
      LisbethMo.github.io
    - 然后在我的demo文件夹里，用 npm install -g hexo-cli 命令安装了
      Hexo
    - 执行命令 hexo init myBlog 初始化
    - 用 cd myBlog 命令进入文件夹
    - 用 npm i 安装依赖
    - hexo new （第一个博客的名字），然后出现了一个md文件的路径
    - 我用 cd 命令进入了那个目录， 然后用 start xxxx.md，编辑这个md文
      件。
    - 几次 cd ..命令回到根目录，然后用 start _config.yml 命令编辑网站
      设置，其中：
	- 把第6行的title改成了myBlog
	- 把第9行的author改成了我自己的名字
	- 把最后一行的 type 改成了 type: git
	- 在最后一行，和type对齐，加上了我的仓库地址 repo: 仓库地址
    - 用 npm install hexo-deployer-git --save 命令安装 git 部署插件
    - 用 hexo deploy 命令启用
    - 然后我进入了我的github网站，打开对应repo，然后在settings里面找到
      了我的链接，将它复制到描述里
    - 最后进入了我的博客

  2、换主题

    - 根据老师的教程，进入了一个主题网站，试了很多个主题，都感觉没有合
      适的，最后试了老师推荐的那个主题
    - 复制了它的 SSH 地址
    - 到我的myBlog文件夹里，使用 cd themes 命令进入主题文件夹
    - 用 git clone 地址 命令将主题下载下来
    - 用 cd ..命令回到上一个目录
    - 把 _config.yml 文件里的 theme 改成我要的那个主题的名字
    - 用 hexo generate 命令生成静态文件
    - 用 hexo deploy 命令将网站部署到服务器上
    - 要稍等一会儿才会出现我的新界面

  3、上传源代码

    - 我在我的 GitHub 里建了一个新repo，叫 blog-generator
    - 打开git bash，在我的myBlog目录里按照新建项目的命令执行
    - 然后用 add-commit-push 三个步骤，生成了我的博客的代码
    - 以后每次 hexo deploy 更新我的博客之后，我都会按照这三个步骤上传
      我的代码到我的 repo 上

以上，就是我用 Hexo 和 GitHub 搭建我的博客系统的全部步骤了
