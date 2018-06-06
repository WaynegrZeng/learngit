mkdir learngit #创建一个目录
cd learngit #打开一个目录  cd /c/Users/WARIZA/learngit
pwd 显示当前目录
git init 把目录变成一个仓库

把文件当到这个目录下面
git add readme.txt 把文件放到这个目录下面
git commit -M"备注" 提交文件，提交后变成最新的版本
git status 工作区与版本库的比较
git diff readme.txt 查看修改的内容

ctrl+d 可以退出未完成的指令

原理： 将修改add到缓存区，再commit到分支上，因此如果修改后没有add，那么commit了也没用，就白做了

git log 打开版本信息
git log --pretty=oneline 打开简略的版本信息

git reset --hard HEAD^(or HEAD~1) 版本回退，并且此时log将不再显示该时点后续的版本序列号

git reflog 查看历史版本信息（帮助回到最新版本）

git checkout -- readme.txt 撤销修改，工作区回到最近的暂存区或版本库的状态

git reset HEAD readme.txt 可以把暂存区的内容撤销掉，放回工作区

Changes not staged for commit:还在工作去 
Changes to be committed:在缓存区，可以提交

本地版本库，远程版本库

rm readme.txt 工作区文件删除
git rm readme.txt + git commit -m"" 组合效果： 版本库删除
工作区的删除可以通过回到版本库的状态找回文档

远程仓库： 好在这个世界上有个叫GitHub的神奇的网站，从名字就可以看出，这个网站
就是提供Git仓库托管服务的，所以，只要注册一个GitHub账号，就可以免费获得Git远程仓

git remote add origin https://github.com/WaynegrZeng/learngit.git 关联PC与远程库
git push -u origin master 关联本地的master分支与远程库origin
以后git push origin master，就可以把最新修改推送到origin

git clone git@github.com:WaynegrZeng/hello-world.git远程库到本地的当前目录
ssh支持的远程git协议传输速度最快

分支在实际中有什么用呢？假设你准备开发一个新功能，但是需要两周才能完成，第一周你写了50%的代码，
如果立刻提交，由于代码还没写完，不完整的代码库会导致别人不能干活了。如果等代码全部写完再一次提交，
又存在丢失每天进度的巨大风险。
Git的分支是与众不同的，无论创建、切换和删除分支，Git在1秒钟之内就能完成！无论你的版本库是1个文件还是1万个文件

git checkout -b dev=git branch dev+git checkout dev
git branch 查看分支

