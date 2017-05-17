### Git常用命令

1. git init 初始化git目录，使该目录变成git可以管理的目录

2. git status 随时掌握工作区的状态，可以看到哪些文件被修改了

3. git add  用该命令告诉Git，把哪些文件添加到仓库，可反复多次使用，添加多个文件

> warning: LF will be replaced by CRLF in xxxx.
The file will have its original line endings in your working directory.

产生该warning的原因：换行符号的不统一 ，windows下的换行符为CRLF，解决方案：

	git config --global core.autocrlf  false

4. git commit -m "本次提交的说明，最好是一些方便阅读的文案"

5. git diff   顾名思义就是查看difference，看本次修改的内容与上次保存文件之间的difference