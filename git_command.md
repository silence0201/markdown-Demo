#Git

1. Create
---

克隆一个存在的仓库

	git clone ssh://user@domain.tld/repo.git
	
递归地复制现有的仓库和所有子模块

	git clone --recursive ssh://user@domain.tld/repo.git
	
创建一个本地仓库

	git init 
	
2. Configuration
---
设置你的名字

	git config [--global] user.name <name>
	
设置你的邮箱
	
	git config [--global] user.email <email>
	
设置命令行颜色

	git config --global color.ui auto
	
查看你的名字

	git config [--global] user.name
	
查看你的邮箱
	
	git config [--global] user.email
	

3. Local Changes
---
显示本地文件的状态

	git status
	
显示改变的内容

	git diff
	
添加当期的改变到下一个提交

	git add <file>
	
添加所有的更改到下一次提交

	git add .
	
重命名并添加到提交

	git mv <file> <new file name>
	
删除并添加到提交

	git rm <file>
	
提交本地所有改变

	git commit -a
	
4. Commit History
---
显示所有提交

	git log
	
显示文件的更改记录

	git log -p <file>
	
显示某人的更改记录

	git log --author=<committer name>
	
根据更改信息查找

	git log --grep=<string>
	
查看文件的每个部分是谁修改的

	git blame <file>
	
暂时存储更改(入栈)

	git stash
	
移除暂时的存储(出栈)

	git stash pop
	
移除上一个提交但是保留本地

	git rm --cached <file>
	
5. Branches & Tags
---
显示存在的分支

	git branch
	
切换分支

	git checkout <branch>
	
创建分支

	git branch <new-branch>
	
基于远程的分支创建分支

	git branch --track <new-branch> <remote-branch>
	
删除本地分支

	git branch -d <branch>
	
删除远程分支

	git push origin --delete <branch>
	
重命名本地分支

	git branch -m <old name> <new name>

重命名远程分支

	git push <remote> :<old name>
	git push <remote> <new name>
	
给当前提交添加标志

	git tag <tag-name>
	
6. Update & Publish
---
显示当前远程的配置

	git remote -v
	
显示远程的信息

	git remote show <remote>
	
创建一个远程仓库

	git remote add <remote> <url>
	
重命名远程仓库

	git remote rename <old-name> <new-name>
	
下载远程的改变,但不进行合并

	git fetch <remote>
	
合并远程仓库

	git pull <remote> <branch>
	
将本地更改推送到远程

	git push <remote> <branch>
	
7. Merge & Rebase
---
合并分支

	git merge <branch>
	
从上游分支获取最新commit信息，并有机的将当前分支和上游分支进行合并

	git rebase <branch>

完全取消变基

	git rebase --abort
	
8. Undo
---
抛弃本地所有更改

	git reset --hard HEAD
	
抛弃本地指定文件的更改

	git checkout HEAD <file>
	
重置到指定提交

	git revert <commit>
	
重置指定文件到指定提交

	git checkout <commit> <file>
	
	