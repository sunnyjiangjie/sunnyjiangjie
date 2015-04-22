---
layout: post
title: 第一篇日志!
---
从最开始想通过Django，自己做搭建一个博客网站，但到最后却因为加载CSS的时候出了问题，查了许久资料，解决了CSS加载的问题，却又发现站点管理的CSS丢了，原因好像就是出在解决CSS加载的代码上。。。到最后就懒得做了。
然后发现可以通过github和Jekyll来搭建不限流量的博客网站，好像还蛮简单的。

然后根据这篇博客：http://blog.fens.me/jekyll-bootstarp-github/  一步一步在本地运行了起来，但之前以为没有搞懂git的用法，一直push不上去，到现在就直接fork一个jekyll的模板，也就现在用的这个。现在的这个下载到本地后，居然不能用jekyll运行，总是出错，也就意味着我不能在本地预览了。
其实我最初的意愿是想自己DIY一个，但现在还没搞懂jekyll，这个以后再慢慢做吧。

现在先把昨天学到的git的一些用法记录一下，免得忘掉。

参考的这篇**[博文](http://blog.csdn.net/steven6977/article/details/10567719)**

【第三步】上传README.md文件

这个时候，我们的GitHub文件夹下就多了一个myRepoForBlog文件夹，进入文件夹目录，对仓库进行初始化，如果我们之前没有勾选创建README，则要先创建README.md文件，不然上传文件会报错。如果在第一步就勾选过了README.MD，则可以直接进入[第四步]

git init

touch README.md

git add README.md

git commit -m 'first_commit'

git remote add origin https://github.com/yourgithub/yourRepo.git

git push origin master

【第四步】push文件

创建完README.md后，就可以push了，代码类似。

`git add .`

`git commit -m 'first_commit'`

`git remote add origin https://github.com/yourgithub/yourRepo.git`

`git push origin master`


如果执行`git remote add origin https://github.com/yourgithub/yourRepo.git`，出现错误：

　　`fatal: remote origin already exists`

则执行以下语句：

　　`git remote rm origin`

再往后执行`git remote add origin [https://github.com/findingsea/myRepoForBlog.git](https://github.com/findingsea/myRepoForBlog.git) `即可。

在执行`git push origin master`时，报错：

　　`error:failed to push som refs to.......`

则执行以下语句：

　　`git pull origin master`

先把远程服务器github上面的文件拉先来，再push 上去。

 　　【结束】


总之我是这样写的：

`先CD到你要同步的文件夹下`


`git remote set-url origin git@github.com:bsspirit/jekyll-demo.git`

`git add .   #加载当前文件夹`

`git commit -m 'new_post' #这个new_post是git用记录更新的，无所谓写什么`

`git pull origin master`

`git push origin master`

在引用图片的时候，可以使用图床网站提供的外链。可以在根目录下建一个images的文件夹，把图片放在里面，比如引用images下面的config.png的方式如下：
`![_config.yml]({{ site.baseurl }}/images/config.png)`

 下面这张图片是做测试的：
![_config.yml]({{ site.baseurl }}/images/dabai.png)
