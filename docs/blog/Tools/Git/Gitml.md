


一、git remote add origin的基础

使用“git remote add origin”指令，可以轻松地将本地项目连接到远程Git仓库
二、git remote add origin的用法

“git remote add origin”指令可以使用以下语法：

    git remote add origin <远程Git仓库地址>

其中，<远程Git仓库地址>是你的远程Git仓库的网址。

对于如何获取远程Git仓库地址，我们举例说明：

比如，你的远程Git仓库地址为：

https://github.com/your/your.git

那么你在本地使用“git remote add origin”指令的语法就应该是：

    git remote add origin https://github.com/your/your.git

执行这条指令之后，你的本地项目就与远程Git仓库建立了连接，你就可以开始对你的代码进行版本追踪和协作开发了。
三、git remote add origin的一些常用操作
1. 更改默认的远程仓库

在项目中可能存在多个远程仓库，如果你想更改默认仓库，可以使用如下指令：

    git remote set-url origin <新的远程Git仓库地址>

2. 查看当前的远程仓库

如果你想查看当前项目的远程仓库，可以使用如下指令：

git remote -v

3. 删除远程仓库

如果你需要删除已经添加的远程仓库，可以使用如下指令：

    git remote rm origin
————————————————












git clone 复制的连接
③下拉仓库

git clone 复制的连接

④将mkdocs生成的项目my-project移到仓库文件夹内

⑤上传

git add .
# 加入到暂存区

git commit -m up
# 提交到版本库

git push
# 上传








# Github

…or create a new repository on the command line

echo "# mk-wiki" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/ryan6981/mk-wiki.git
git push -u origin main

…or push an existing repository from the command line

git remote add origin https://github.com/ryan6981/mk-wiki.git
git branch -M main
git push -u origin main













引言

Git 和repo 极简操作指南小结…
一、Git 基本操作
1、下载拷贝代码
1.1、git clone ssh:// 或者https：// 从代码仓库拷贝

    复制指定单一分支

    git clone -b <branch-name> --single-branch https://xxx/xx/repo.git
        1

git clone git@xxx:main/xx.git --depth=1 --branch=release-client-5.11.x --single-branch


- 拷贝最新一次提交

```shell
git clone --depth=1 https://xxx/xxxx/repo.git

    1
    2
    3
    4
    5

1.2、git pull 和git fetch 同步更新

git pull <远程主机名> <远程分支名>:<本地分支名>


git fetch <远程主机名> <远程分支名>:<本地分支名>

    1
    2
    3
    4

    git pull —— 使用给定的参数运行git fetch，并调用git merge将检索到的分支头合并到当前分支中即git pull= git fetch +git merge

    # 将远程主机origin的master分支拉取过来，与本地的brantest分支合并
    git pull origin master:brantest
        1
        2

    git fetch——不会进行合并执行后需要手动执行git merge合并分支

2、提交代码
2.1、git status 查看本次修改的情况

    repo的话用 repo status

2.2、git diff --cached 查看暂存区和本地最近的版本 (commit) 的 不同 和 git diff HEAD 查看工作区、暂存区 和本地最近的版本 (commit) 的 different (不同)
2.3、git add 添加修改到暂存区和git rm --cached将修改从暂存区移除

git add .
git add file.txt file1.java xxx.x
git rm --cached file.txt file1.java xxx.x

    1
    2
    3

2.4、git commit 提交本次修改到本地仓库 / git commit --amend 修改最近一次 commit 的描述

git commit --amend 可以更新最近一次commit的描述，如果此次有修改也会顺道把此次新增的修改一道commit。
2.5、git push

推送到远端代码仓库

#把本地当前的分支push到原创origin 的临时分支mutl_volume （不需要先创建临时分支）
git push origin HEAD:refs/heads/mutl_volume

    1
    2

3、回退本地仓库代码
3.1、git reset

    git reset—— 撤销当前暂存区的修改，即撤销当前add 操作

    git reset --hard < HEAD > 或 < commitId > ——放弃当前的修改，也可以用于放弃制定commitId的修改（默认-mixed参数），一般用于未push到远程代码仓库的本地修改，即撤销暂存区的修改，抛弃当前的修改。

    git reset – mixed HEAD^ ——回退至上个版本，它将重置HEAD到另外一个commit,并且重置暂存区以便和HEAD相匹配，但工作区不会被更改。

    git reset – soft HEAD~3 ——回退至三个版本之前，只回退了commit的信息，暂存区和工作区与回退之前保持一致，如果还要提交，直接commit即可

    reset 命令会抹去某个 commit id 之后的所有 commit

3.2、git revert commitId 抹掉某个commit的修改

回退具体的某个commitId，用于紧急回退到某个有问题的提交，以新增一个 commit 的方式还原某一个 commit 的修改
3.3、git checkout

回退到历史的某个节点，通常用于代码整体回退到某个历史节点，回退某个文件或者回退到上一个分支。

git checkout file1 file2
git checkout .
git checkout -

    1
    2
    3

4、同步代码
4.1、git cherry-pick

同步单个节点
4.2、git merge

同步整个分支
4.3、git pull
4.4、git rebase（不推荐的方式）

同步整个分支。
6、git branch分支管理

    git branch -r —— 列出所有远程分支
    git branch -a ——查看所有分支
    git checkout —— 切换分支
    git checkout -b < new_branch >—— 创建并切换到本地新分支
    git checkout -b < branch-name > origin/< branch-name >——从远程分支中创建并切换到本地分支
    git merge —— 合并分支
    git branch –d —— 删除本地分支
    git push origin --delete < remote-branch > 或 git push origin :< remote-branch >——删除远程分支
    git remote prune origin——远程删除了分支本地也想删除
    git branch -m < new-branch >——重命名本地分支

7、git tag

    git tag < version-number > 或 git tag -a —— 添加标签

    默认 tag 是打在最近的一次 commit 上，如果需要指定 commit 打 tag

    git tag -a <version-number> -m "v1.0 发布(描述)" <commit-id>
        1

    git describe --tags --abbrev=0 ——展示当前分支的最近的 tag

    git tag -l —— 查看标签

    git tag -d < tagname >—— 删除本地标签

    git push origin --delete tag < tagname >—— 删除远程标签

    git checkout -b branch_name tag_name——切回到指定分支的指定tag

    git push origin --tags——推送本地所有标签到远程服务器

8、git stash 或者git apply 江湖救急，临时保存一下代码

如果现有的修改需要保留，则可以参考临时保存一下代码的方法，全部add，commit，然后使用本地分支保存。

git add --all
git commit -s 
git checkout -b new_temp_branch
git checkout 原来的分支   或者 使用repo sync -d .

    1
    2
    3
    4

    git stash的内部原理其实也就是临时分支的方法即git checkout -b

将代码保存到临时分支，那么保存后如何回到原来的分支呢？如果是repo管理的仓库，则使用命令 repo sync -d .，当然也可以使用下面的git checkout命令，如果是纯git管理的仓库，则使用命令git checkout 原来的分支，临时分支使用完毕后，如果要删除，则 git branch -D 临时分支名。
9、git reflog +git cherry-pick 乾坤大挪移，找回丢失的节点和迁移代码

git也有回收站机制，凡是只要commit过的节点，都可以通过git reflog命令查看提交记录，

@yanfa200_ubuntu14-nas-18115:jdk8-181009:~/crazymo/forWork/LocationService$ git reflog
7a1903d HEAD@{0}: pull: Merge made by the 'recursive' strategy.
aa903dc HEAD@{1}: commit: fixed merged ag
d453eee HEAD@{2}: commit (merge): fixed merged
303f231 HEAD@{3}: commit: 内部逻辑优化
2cf9db3 HEAD@{4}: commit: 合并完成，进行内部优化前的备份
1a141c7 HEAD@{5}: clone: from git@yfgitlab.crazymo.com:MSDD/Service/LocationService.git

    1
    2
    3
    4
    5
    6
    7
    8

如上所示可以看到所有的文件上传到暂存区的操作记录：假如要想找回的是{3}对应的提交那么有两种方式：
9.1、reset Head@{3} 配合 git reset --hard HEAD

    首先git reset Head@{3} 将头指针指向{3}索引处
    再git reset --hard HEAD 找回

9.2、git cherry-pick 某节点hash

    git cherry-pick 某节点hash

git cherry-pick的时候，有时会提示有冲突，则按照git 解冲突的方法，修改好代码，并git add 提交到暂存区。然后执行 git cherry-pick --continue方法即可，通过git reflog + git cherry-pick, 我们就可以轻松找回那些任何前面提交过的节点。
10、重复利用被abandon 的commit
废物利用——如何处理被abandon的提交点

代码提交过程中，由于是多人协作，容易出现因为代码冲突或者其他原因导致代码无法合入，而被评审人abandon。这种情况下，如何尽可能利用既有的提交节点呢？
10.1. 更新本地代码到最新服务器节点

如果是repo管理下的仓库

    repo sync -d .

如果是单git仓库，

    git reset --hard #hash节点是被abandon的节点的父节点。

    git pull

扩展：为什么要更新代码？更新代码的目的是为了与服务器保持一致，才不容易造成冲突。
10.2. 找回被abandon的点

基于[乾坤大挪移手法](#git reflog +git cherry-pick 乾坤大挪移，找回丢失的节点和迁移代码)，找回被abandon的点，并合并到最新的代码上。
10.3. 重新修改代码并提交

根据abandon原因，做相应的代码修改。修改完成后，使用以下命令，完成代码提交

    git commit --amend #注意，必须加选项–amend, 要不然就是新增一个commit了，在配合Gerrit使用时提交信息中注意删除change-id信息，不然提交评审时会直接被打回。

Description: add setSystemCurrentTimeHookEx Function to support setCurrentTime with millsecond
Solution   :
Notes      :

Change-Id: Id0992cd0a79720d6922fb59b8d9070a1efd23400  # 这一行必须删除

    1
    2
    3
    4
    5

11、git rm 将文件从暂存区中移除

git rm 命令相当于直接删除文件并将该操作add到暂存区，所以就相当于直接从暂存区移除指定文件。
11.1、git rm --cached 从暂存区移初之前已经add 过的文件

    -r——表示移除的是目录

当需要在移除版本控制中的指定文件并需要在工作区中保留该文件时，需要带–cached 参数。常用于git忽略已经被提交过的文件，先git rm --cached <file>，然后更新.gitignore忽略掉目标文件，最后git commit -m。
12、多项目并行开发

只有一份代码，如何实现多项目并行开发，比较优雅的方法，创建本地分支。
11.1、本地分支法
11.1.1、 基于远程分支，创建一个本地分支

    git checkout -b XXX origin/XXX

一般我们推荐本地分支名和远程分支名一样，直观好理解。基于分支进行多项目并行开发时，切记切换前保证代码是干净状态。
11.1.2、保存工作了一半的成果到本地分支

干了一半，需要切换到其他分支，则直接将修改的代码全部添加提交。注意，只是commit，不push到远程代码服务器。
11.1.3、 切换到其他项目的分支

    git checkout -b YYY origin/YYY

如果原来YYY已经创建好了，则直接git checkout YYY即可，不需要新建分支。
二、配置commit 命令自动补全和提交模板
1、配置git命令自动补全

将git_completed文件放置到编译服务器用户根目录下，并修改根目录下的.profile 或者 .bashrc文件

增加下面代码 source ~/git_completed，git_completed文件内容见附件
2、配置提交注释模板

将commit-msg.template.txt放置到编译服务器用户根目录下，并执行下面命令，git config --global commit.template ~/commit-msg.template.txt
3、配置用户名和邮件

git config --global  user.email  <email>
git config --global  user.name  <name>

    1
    2

4、Git 中文乱码解决
4.1、git status 乱码

git config --global core.quotepath false
4.2、git commit 乱码

git config --global i18n.commitencoding utf-8
4.3、git status 乱码

git config --global i18n.logoutputencoding utf-8
————————————————

                            版权声明：本文为博主原创文章，遵循 CC 4.0 BY 版权协议，转载请附上原文出处链接和本声明。
                        
原文链接：https://blog.csdn.net/CrazyMo_/article/details/115278670
