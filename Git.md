# Git
-----------------------------

####三个用户体验很棒的 Git 学习网站 
- [Try git](https://try.github.io/levels/1/challenges/1) 
	- [Github 代码托管地址](https://try.github.io/levels/1/challenges/1) 
- [Git Tutorial](https://www.codeschool.com/courses/git-real)  
- [界面演示操作](http://pcottle.github.io/learnGitBranching/) 
	- [Github 代码托管地址](https://github.com/pcottle/learnGitBranching)
！[](https://camo.githubusercontent.com/d06d3d418bf649123baa5dd9b10c2187e048aa60/68747470733a2f2f7261772e6769746875622e636f6d2f70636f74746c652f6c6561726e4769744272616e6368696e672f6d61737465722f6173736574732f6c6561726e4769744272616e6368696e672e706e67)
![](https://camo.githubusercontent.com/d06d3d418bf649123baa5dd9b10c2187e048aa60/68747470733a2f2f7261772e6769746875622e636f6d2f70636f74746c652f6c6561726e4769744272616e6368696e672f6d61737465722f6173736574732f6c6561726e4769744272616e6368696e672e706e67)




###1 [<Strong>Git版本回退操作</strong>](http://hi.barretlee.com/2014/04/28/git-roll-back/)

	git log

	commit bcdfd65ba3f16a0647e7687f92cca25d51738d2e  
	Author: Barret Lee <barret.china@gmail.com>  
	Date:   Mon Apr 28 01:22:27 2014 +0800  

    now post  

	commit 69eeaa60c5808c143aabce4d52feb104e2e4591b  
	Author: Barret <barret.china@gmail.com>  
	Date:   Sat Apr 26 21:03:48 2014 +0800  

    fix bug
	....



	git reset --hard SHA 

	...
	git push -u master origin

	...
	git push -u master origin -f
>git回到上一版本命令
 
>git reset是指将当前head的内容重置，不会留log信息。
 
>git reset HEAD filename  从暂存区中移除文件
 
>git reset --hard HEAD~3  会将最新的3次提交全部重置，就像没有提交过一样。
 
>git reset --hard commit (38679ed709fd0a3767b79b93d0fba5bb8dd235f8) 回退到 38679ed709fd0a3767b79b93d0fba5bb8dd235f8 版本
 
>根据--soft --mixed --hard，会对working tree和index和HEAD进行重置:
 
>git reset --mixed：此为默认方式，不带任何参数的git reset，即时这种方式，它回退到某个版本，只保留源码，回退commit和index信息
 
>git reset --soft：回退到某个版本，只回退了commit的信息，不会恢复到index file一级。如果还要提交，直接commit即可
 
>git reset --hard：彻底回退到某个版本，本地的源码也会变为上一个版本的内容
例如：我要彻底返回在上一次提交以前的版本。git reset --hrad HEAD~1
 
>我要回到上一次提交的版本：
 
><strong>git reset --hard</strong>  



###2 [<Strong>Git for mac 中文乱码</strong>](http://www.cnblogs.com/perseus/archive/2012/11/21/2781074.html)


    git stataus .
    然后中文乱码

    modified:   Git/vi/274\232\350\256\256\346\200\273\347\273\223.pdf 

#####解决方案：

在bash提示符下输入：

`git config --global core.quotepath false`   
######core.quotepath设为false的话，就不会对0×80以上的字符进行quote。中文显示正常。



###2 [<Strong>Git rebase</strong>](http://www.cnblogs.com/kym/archive/2010/08/12/1797937.html)

[git rebase 用法](http://blog.csdn.net/wangjia55/article/details/8776409)  
[git rebase 运行过程分析](http://blog.csdn.net/hudashi/article/details/7664631)  




###2 [<Strong>git blame</strong>](http://www.techug.com/10-tips-git-next-level)
>[Git 10个小贴士](http://www.techug.com/10-tips-git-next-level)


`git blame [file_name]`  
>查看文件被谁修改过



###2 [<Strong>gitrm --cached</strong>](http://www.sitepoint.com/git-for-beginners/)

`git rm --cached [file_name]`  

>删除缓存文件

`git show <hash>`  

>查看 hash文件修改内容


`git log --graph --all`  

>查看提交历史log 图表