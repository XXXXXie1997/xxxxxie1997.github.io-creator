---
title: "如何用 hugo 搭建个人博客"
date: 2020-04-11T11:02:10+08:00
draft: false
---

1. 首先当然是安装hugo了^_^。安装完后运行`hugo version`可以检查是否成功安装

2. 通过运行`hugo new site xxxx.github.io-creator`在当前目录下建立新的hugo目录，名为xxxx.github.io-creator **（xxxx为github用户名，全小写。）**

3. 进入xxxx.github.io-creator目录，在目录中建立git库(`git init`)

4. 运行`git submodule add https://github.com/budparr/gohugo-theme-ananke.git themes/ananke`，从github下载名为ananke的主题

5. 运行`echo 'theme = "ananke"' >> config.toml`，将主题信息添加到配置文件中

6. 运行`hugo new post/blog01.md`，在当前目录下的post目录中新建 blog01.md

7. 进入post目录中，运行`code blog01.md`，打开blog01进行编辑

8. 修改title为任意内容，draft属性改为false（draft属性决定文件是否保存为草稿）

9. 哒哒哒的码入内容……

10. 码完保存后，运行`hugo -D`建立页面，该页面会以文件夹的形式出现在xxxx.github.io-creator/public/post中

11. 运行`hugo server`，启动hugo服务器（也可以省略步骤10，运行`hugo server -D即可），便可从本地查看页面效果。若要配置新主题，需自行琢磨。。

12. 回到xxxx.github.io-creator目录，运行`touch .gitignore`并打开，将public文件夹输入，从git本地库中忽视该文件夹

13. 访问[github](https://github.com/)，建立新的远程库，名为xxxx.github.io **（xxxx同样为用户名小写，不能出错）**

14. **进入public目录**

15. 复制远程库SSH地址，运行`git remote add oringin SSH地址`将本地库public与远程库xxxx.github.io联系起来

16. 运行`git push -u xxxx.github.io master`，将本地public中的内容上传至github

17. 进入setting，可以看到链接[http://xxxx.github.io//](http://xxxx.github.io//)，这就是上传至public的博客页面了

如果要添加新的博客，按以下步骤：

1. 回到xxxx.github.io-creator目录下，运行`hugo new post/aaaaa.md`

2. 打开aaaaa.md

3. 修改属性，码字，保存

4. 运行`hugo -D`在public中生成页面

5. `ga .` `gc` `gp`三连送上，就完成了博客的更新