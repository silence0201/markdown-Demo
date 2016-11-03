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
	


