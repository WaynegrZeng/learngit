mkdir learngit #创建一个目录
cd learngit #打开一个目录
pwd 显示当前目录
git init 把目录变成一个仓库

把文件当到这个目录下面
git add readme.txt 把文件放到这个目录下面
git commit -M"备注" 提交文件，提交后变成最新的版本
git status 查看仓库与上一次commit时对比的状态
git diff readme.txt 查看修改的内容

ctrl+d 可以退出未完成的指令

原理： 将修改add到缓存区，再commit到分支上，因此如果修改后没有add，那么commit了也没用，就白做了

git log 打开版本信息
git log --pretty=oneline 打开简略的版本信息

git reset --hard HEAD^(or HEAD~1) 版本回退，并且此时log将不再显示该时点后续的版本序列号

git reflog 查看历史版本信息（帮助回到最新版本）

git checkout -- readme.txt 撤销修改，回到最近的暂存区或版本库的状态