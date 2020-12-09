# Git

### Git是目前世界上最先进的分布式版本控制系统（没有之一），由C语言开发

### Linux系统上下载Git(Ubuntu)

```bash
sudo apt-get install git
```

#### 安装完成后进行设置:

```bash
git config --global user.name "Your Name"
git config --global user.email "email@example.com"
```

### 创建版本库(repository)

#### 可以简单理解为一个目录，其中所有文件都可被Git管理起来

#### 每个文件的修改、删除，Git都能追踪或还原

##### 1.创建一个空目录

```bash
mkdir learngit	#创建一个目录learngit
cd learngit	#切换到目录learngit下
pwd	#显示当前目录
/home/rulerscourt/learngit
```

##### 2.将此目录变成Git可以管理的仓库

```bash
git init	#Git建立仓库并告诉你这是一个空仓库(empty Git repository)
Initialize empty Git repository in /home/rulerscourt/learngit/.git/	#bash中没有initialize这个命令，我也不知道这句到底干嘛的，目前来看不输入也不会影响什么
ls -ah	#可以看见隐藏的.git目录，是Git用来跟踪管理版本库的，不要手动修改此目录内的文件
```

##### 3.把文件添加到版本库

###### 注：

###### 所有版本控制系统，只能跟踪文本文件的改动，如TXT，网页，程序代码等

###### 但所有的二进制文件如图片视频Word格式文档，可以由版本控制系统进行管理，但无法跟踪文件的变化

###### 建议所有语言使用同一种标准的UTF-8编码

##### 建立一个readme.txt文件，内容如下：

###### Git is a version control system.

###### Git is free software.

##### 一定将此文件放至learngit目录或其子目录下

```bash
git add readme.txt	#告诉Git将文件添加到仓库
git commit -m "wrote a readme file"	#告诉Git把文件提交到仓库；-m后面输入的是本次提交的说明
[master （根提交） e5ad229] wrote a readme file
 1 file changed,2  insertions(+)
 create mode 100644 readme.txt
#这是命令成功后所反馈给你的信息：
#一个文件被改动(即我们新添加的readme.txt文件)
#插入了两行内容(即我们所写的readme.txt有两行内容)
```

##### commit可以一次提交很多文件，可多次add不同的文件

```bash
git add file1.txt
git add file2.txt file3.txt
git commit -m "add 3 files"
```

#### 4.时光穿梭

##### 继续修改readme.txt文件：

###### Git is a distributed version control system.

###### Git is free software.

##### 查看结果：

```bash
git status
位于分支 master
尚未暂存以备提交的变更：
  （使用 "git add <文件>..." 更新要提交的内容）
  （使用 "git checkout -- <文件>..." 丢弃工作区的改动）

	修改：     readme.txt

修改尚未加入提交（使用 "git add" 和/或 "git commit -a"）
#此命令可以让我们时刻掌握仓库当前状态，比如上面就很贴心的提示我们readme.txt已经修改了但尚未有准备提交的修改
```




