### Git常用命令

1. git init 初始化git目录，使该目录变成git可以管理的目录

2. git status 随时掌握工作区的状态，可以看到哪些文件被修改了

3. git add  用该命令告诉Git，把哪些文件添加到仓库，可反复多次使用，添加多个文件

    warning: LF will be replaced by CRLF in xxxx.
    The file will have its original line endings in your working directory.

产生该warning的原因：换行符号的不统一 ，windows下的换行符为CRLF，解决方案：

    git config --global core.autocrlf  false

4. git commit -m "本次提交的说明，最好是一些方便阅读的文案"

5. git diff   顾名思义就是查看difference，看本次修改的内容与上次保存文件之间的difference

6. git log  查看代码的提交日志
 
7. git log --pretty=oneline  将每次提交的日志纪录显示在一行，方便查看

8. git reset --hard  commitId  切换到某一次提交

9. git reflog   当git reset时，发现commitId无法找到了，使用reflog可以查看历史命令，以便确定要回到未来的哪个版本

10. git checkout -- filename  把readme.txt文件在工作区的修改全部撤销

一种是readme.txt自修改后还没有被放到暂存区，现在，撤销修改就回到和版本库一模一样的状态；

一种是readme.txt已经添加到暂存区后，又作了修改，现在，撤销修改就回到添加到暂存区后的状态。

总之，就是让这个文件回到最近一次git commit或git add时的状态。

11. git reset HEAD filename   把file从缓存区撤回到工作区中

12. git rm filename   从版本库中删除文件 

13. git remote add origin xxxx  添加一个远程仓库

14. git clone xxxxxxxxxxxxx 克隆一个仓库到本地

15. git checkout -b $branchName   新建分支并切换

16. git branch 查看当前分支

17. git merge  $branchName 合并指定分支到当前分支

18. git branch -d $branchName  删除分支

19. git branch -D $branchName  强行删除分支，不管是否合并过

19. git stash  把当前工作现场“储藏”起来，等以后恢复现场后继续工作, 场景 ： 正在做一个任务，突然有个bug过来，要新建一个分支处理

20. git stash list 查看工作区列表，恢复工作区的时候有用

21. git stash apply 恢复工作现场，但列表中的工作区还在

22. git stash drop 删除工作现场

22. git stash pop   == git stash apply + git stash drop