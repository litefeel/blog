---
layout: post
post_title: "笔记：Git Essential Training"
post_date: 2015-06-22 18:20
published: false
tags: [笔记,前端]
categories: 编程
---
 
# 1. 什么是Git
## 1.1 Understanding version control
1. Keep track of changes
	- 特别是text changes
	- v1，v2，v3
2. version control system
3. 主要就是为了 source code management 
4. 无论如何，做图片，做文档，做wiki，我们都和版本控制有关，常常的都和ctrl+z的撤销的操作有关

## 1.2 The history of Git
1. Source code control system，1972 免费在unix提供
2. revision contrl system，open source，1982 可以在windows上使用
3. concurrent versions system，1986-1990，open source
4. apache subversion（SVN），2000 open source，备份这个文件树，而不是单个文档，即便更名了也可以track
5. bitkeeper scm
	- 2000 closed source，proprietary
	- community version was free
	- distributed version control
	- used fr source code of the linux kernel from 2002-2005
	- controversial to use proprietary scm for an open source project
	- april 2005, the comunicty version is not free
6. git was born
	- april 2005
	- ctreate by linus torvalds
	- distributed version control
	- open source and free software
	- conpatible with unix-like sytems and windows
	- faster than other scms(100x) 

## 1.3 About distributed version control
1. 加入我们对一个文档做了A B C D的4个系列的小修改
2. 你可以恢复到只做了ABC修改的文档，也可以恢复到只做了CD修改的文档
3. 好处是：no need to communicate with central server
	- faster 
	- no network access required
	- no single failure point 
4. encorages the participation and forking or the project	- developers can work independently
	- submit change sets fr inclusion and rejection
5. 没有conral repositary的概念

## 1.4 Who should use Git?
1. 只要需要监控基于文档修改的人都可以用git，不一定是开发者


# 2. 安装Git

## 2.1 Installing Git on a Mac
- [下载地址](http://git-scm.com/book/zh/v1/%E8%B5%B7%E6%AD%A5-%E5%AE%89%E8%A3%85-Git)

## 2.2 Installing Git on Windows

## 2.3 Installing Git on Linux
## 2.4 Configuring Git
1. system 层面的配置，影响每一个用户
	- UNIX：/etc/gitconfig
	- windows:program files\git\etc\gitconfig
	- 命令：git config --system
2. 	user层面的配置
	- ~/.gitconfig
	-$home\.gitconfig
	- 命令：git config --global
3. project
	- my_project/.git/config 	
	- 命令：git config
4. 具体配置

		git config --global user.name "Ben Wang"
		git config --global user.email "xx@gmail.com"
	
		cd ~ #进入用户目录
		ls -la 显示文件夹目录
		cat .gitconfig # 可以模拟以文档显示的模式打开config文件
		git config --global core.editor "subl -n -w"  #设置默认的文本编辑器
		
5. 查看配置信息：要检查已有的配置信息，可以使用 `git config --list` 命令：

   		$ git config --list
   	 	user.name=Scott Chacon
   		user.email=schacon@gmail.com
    	color.status=auto
    	color.branch=auto
    	color.interactive=auto
    	color.diff=auto
    	...

6. 有时候会看到重复的变量名，那就说明它们来自不同的配置文件（比如 `/etc/gitconfig` 和 `~/.gitconfig`），不过最终 Git 实际采用的是最后一个。

7. 也可以直接查阅某个环境变量的设定，只要把特定的名字跟在后面即可，像这样：

   		$ git config user.name
    	Scott Chacon
		

## 2.5 Exploring Git auto-completion
1. 如何远程下载

		curl -OL https://github.com/git/git/raw/master/contrib/completion/git-completion.bash2. 
		mv ~/git-completion.bash .git-completion.bash # 将文件一栋并设置为为隐藏 tab为自动填写
		
		if [-f ~/.git-completion.bash]; then
			source ~/.git-completion.bash
		fi
		
2. 重命名的规则

		git mv [-v] [-f] [-n] [-k] <source> <destination>
		git mv [-v] [-f] [-n] [-k] <source> ... <destination directory>3. 
		
3. 利用nano编辑bash profile,加载git的自动填写功能

		nano .bash_profile
		
## 2.6 Using Git help

1. git help 显示帮助
2. git help log 显示具体的控制帮助页面介绍，空格查看下一页，f前进，b后退,q退出
3. qit help log 等于man git-log
4. 比如，要学习 config 命令可以怎么用，运行：

		$ git help config

# 3. Getting Started

## 3.1 Initializing a repository
1. 有两种取得 Git 项目仓库的方法。第一种是在现存的目录下，通过导入所有文件来创建新的 Git 仓库。第二种是从已有的 Git 仓库克隆出一个新的镜像仓库来。
2. 在工作目录中初始化新仓库
	- 要对现有的某个项目开始用 Git 管理，只需到此项目所在的目录(进入对应的项目文件夹：cd docuements/first_git_project)，执行：

			$ git init
		
	- 如果当前目录下有几个文件想要纳入版本控制，需要先用 git add 命令告诉 Git 开始对这些文件进行跟踪，然后提交：

			$ git add *.c
			$ git add README
			$ git commit -m 'initial project version'
4. [从现有仓库克隆](http://git-scm.com/book/zh/v1/Git-%E5%9F%BA%E7%A1%80-%E5%8F%96%E5%BE%97%E9%A1%B9%E7%9B%AE%E7%9A%84-Git-%E4%BB%93%E5%BA%93#在工作目录中初始化新仓库)
	- 克隆仓库的命令格式为 git clone [url]。比如，要克隆 Ruby 语言的 Git 代码仓库 Grit，可以用下面的命令：

			$ git clone git://github.com/schacon/grit.git
	- 这会在当前目录下创建一个名为grit的目录，其中包含一个 .git 的目录，用于保存下载下来的所有版本记录，然后从中取出最新版本的文件拷贝。如果进入这个新建的 grit 目录，你会看到项目中的所有文件已经在里边了，准备好后续的开发和使用。如果希望在克隆的时候，自己定义要新建的项目目录名称，可以在上面的命令末尾指定新的名字：

			$ git clone git://github.com/schacon/grit.git mygrit
	- 唯一的差别就是，现在新建的目录成了 mygrit，其他的都和上边的一样。
		
## 3.2 Understanding where Git files are stored
- 进入项目文件，使用ls -la .git打开git的隐藏文件

## 3.3 Performing your first commit
1. make the changes
1. add the changes:git add. 将文件夹内所有的修改都添加到git当中
2. commit the changes  to the repositary with a message : git commit -m  "Initial commit"将修改上传并命名

## 3.4 Writing commit messages
1. best pratice
	-  a single-line summary,less than 50 characters 
	-  Optionally, we can follow that by a blank line and then a more complete description.
	- Even then you want to keep those additional lines to less than 72 characters
	- write commit messages in the present tense, not in the past tense
	- bullet points are usually asterisks or hephens
	- 可以增加ticket number来自于用户的反馈
	- 可以增加前缀，比如[js,css][bugfix]#38054
2. be clear and descriptive
	- bad:fix typo
	- good : add missing > in project section of html
3. 例子
		
		 t23094 - Fixes bug in admin logout. 
		 That's a little bit vague, but we've got something underneath it that gives it more description, When an admin logged out of the admin area, they could not log in to the members area because their session :user_id was still set to the admin ID.4. 	 

## 3.5 Viewing the commit log
- git log 
- 限制最近的log条数：git log -n 1 代表返回log的条数
- 限制log的时间范围：git log --since=2002-06-14	git log --until=2002-06-14
- 限制作者：git log --author=""
- 关键词搜索log:git log --grep="init"

# 4. Git Concepts and Architecture

## 4.1 Exploring the three-trees architecture
1. 传统式two tree，但是git 是three trees：working space - staging index - repository，这样是为了把不同的修改组成一个change set，然后再commit

## 4.2 The Git workflow
1. git add . 和git add file.txt 的区别在于前者是add所有，后者是add具体文件的修改
2. 讲解版本控制的过程

## 4.3 Using hash values (SHA-1)
- SHA 是一个40个字符的识别码，对于change set是唯一的识别码

## 4.4 Working with the HEAD pointer
- 把head比喻成录音的录音键，你可以倒回去，但是一旦开始录音，之前的东西都会被洗掉
- head文件其实在.git里，可以用ls -la

# 5. Making Changes to Files

## 5.1 Adding files
1. 查看branch的状态：git status 可以查看文件夹内没有commit的文件
2. git 命令是这么处理空格的：
		
		Programming\ For\ Everyone.md
3. 忽略某些文件：一般我们总会有些文件无需纳入 Git 的管理，也不希望它们总出现在未跟踪文件列表。通常都是些自动生成的文件，比如日志文件，或者编译过程中创建的临时文件等。我们可以创建一个名为 .gitignore 的文件，列出要忽略的文件模式。来看一个实际的例子：

		$ cat .gitignore
		*.[oa]
		*~

## 5.2 Editing files
1. git add . 
2. git commit
3. git status
4. git log

## 5.3 Viewing changes with diff
1. git diff 是查看对比文档的区别
	- ---表示旧文件，+++表示新文件，@@表示line number 
2. 也可以直接查看每个文档的变化  diff firstfile.txt

## 5.4 Viewing only staged changes
1.若要看已经暂存起来的文件和上次提交时的快照之间的差异，可以用 git diff --cached 命令。（Git 1.6.1 及更高版本还允许使用 git diff --staged，效果是相同的，但更好记些。）来看看实际的效果：

	$ git diff --cached
	diff --git a/README b/README
	new file mode 100644
	index 0000000..03902a1
	--- /dev/null
	+++ b/README2
	@@ -0,0 +1,5 @@
	+grit
	+ by Tom Preston-Werner, Chris Wanstrath
	+ http://github.com/mojombo/grit
	+
	+Grit is a Ruby library for extracting information from a Git repository2.git diff --staged

## 5.5 Deleting files
1. git rm files_to_dielete.txt

## 5.6 Moving and renaming files
1. 2种方法
	- 直接在finder重命名，然后在git提交修改（add——》rm）；
	- 另外一种是直接在git重命名：mv second_file.tx secondary_file.txt

	


