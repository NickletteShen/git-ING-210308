# git-ING-210314 

## 正常流程： 
#### 1.在github主页新建repository  
#### 2.在本地代码文件夹初始化git init  
#### 3.添加远程仓库地址 git remote add origin XXX.git  
! 如果新建repository时添加了readme.md，则需要git pull origin main ，否则会出现坑1  
#### 4.git add .  
#### 5.git commit –m 说明  
#### 6.git push origin master:main  

## 在实践中使用git推代码遇到的坑 
坑（1）   fatal: couldn't find remote ref master
因为在远程仓库有ReadMe文件，而本地没有，造成本地和远程的不同步
因为使用了旧命令master，master现在被认为是有种族歧视的，github将其换成了main

会出现：
 
请输入提交消息来解释为什么这种合并是必要的
git 在pull或者合并分支的时候有时会遇到这个界面。可以不管(直接下面3,4步)，如果要输入解释的话就需要:

1.按键盘字母 i 进入insert模式

2.修改最上面那行黄色合并信息,可以不修改

3.按键盘左上角"Esc"

4.输入":wq",注意是冒号+wq,按回车键即可


（3）	坑2 fatal: unable to access 'https://github.com/NickletteShen/crawlerGovPolicy/': Failed to connect to github.com port 443: Timed out
网站不稳定，不停重复命令，刷新DNS：ipconfig /flushdns
（4）	坑3 

（5）	坑4 慎用强制上传覆盖远程文件git push -f origin master
(这个命令在团队开发的时候可能会有生命危险)

（6）	https://www.cnblogs.com/runnerjack/p/9342362.html
