github的SSH配置

一 、设置Git的user name和email：
$ git config --global user.name "xuhaiyan"
$ git config --global user.email "haiyan.xu.vip@gmail.com"
二、生成SSH密钥过程：
1.查看是否已经有了ssh密钥：cd ~/.ssh
如果没有密钥则不会有此文件夹，有则备份删除
2.生存密钥：
$ ssh-keygen -t rsa -C “haiyan.xu.vip@gmail.com”
按3个回车，密码为空。
最后得到了两个文件：id_rsa和id_rsa.pub

3.添加密钥到ssh：ssh-add 文件名
4.在github上添加ssh密钥，这要添加的是“id_rsa.pub”里面的公钥。
5.测试：ssh git@github.com


三、 开始使用github
1.获取源码：
$ git clone git@github.com:billyanyteen/github-services.git
2.这样你的机器上就有一个repo了。
3.git于svn所不同的是git是分布式的，没有服务器概念。所有的人的机器上都有一个repo，每次提交都是给自己机器的repo
仓库初始化：
git init
生成快照并存入项目索引：
git add
文件,还有git rm,git mv等等…
项目索引提交：
git commit
4.协作编程：
将本地repo于远程的origin的repo合并，
推送本地更新到远程：
git push origin master
更新远程更新到本地：
git pull origin master
补充：
添加远端repo：
$ git remote add upstream git://github.com/pjhyett/github-services.git
重命名远端repo：
$ git://github.com/pjhyett/github-services.git为“upstream”
