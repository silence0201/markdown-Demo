#git

1. git常用指令
---
配置用户名：`git config “user.name” 用户名`（用于跟踪修改记录）  

配置邮箱：`git config “user.email” 邮箱`（用于多人开发间的沟通）  

查看配置信息：`git config –l`

编辑配置信息：`git config –e`（用vim编辑，:wq是退出vim编辑器）

设置指令的别名：`git config alias.别名 原指令名称`

设置带参数指令的别名：`git config alias.别名 “原指令名称 参数”`

将此设置应用到整个系统中：`git config ––gloabal`

2. 状态
---
git status ：查文件的状态  
查看某个文件的状态：git status 文件名  
查看当前路径所有文件的状态：git status  

`git log` ：查看文件的修改日志  
查看某个文件的修改日志：`git log 文件名`  
查看当前路径所有文件的修改日志：`git log`  
用一行的方式查看简单的日志信息：`git log ––pretty=oneline`  
查看最近的N次修改：`git log –N`（N是一个整数）  

`git diff` ：查看文件最新改动的地方  
查看某个文件的最新改动的地方：`git diff` 文件名  
查看当前路径所有文件最新改动的地方：`git diff`  

3. 使用
---
`git init` ：初始化一个空的本地仓库，生成一个`.git`目录，用于维护版本信息  
在当前路径初始化仓库：`git init`  
在其他路径初始化仓库：`git init 仓库路径`  

`git add` ：将工作区的文件保存到暂缓区  
保存某个文件到暂缓区：`git add 文件名`  
保存当前路径的所有文件到暂缓区：`git add .`（注意，最后是一个点 . ）  

`git commit` ：将暂缓区的文件提交到当前分支  
提交某个文件到分支：`git commit -m ”注释” 文件名`  
保存当前路径的所有文件到分支：`git commit -m ”注释”`   

`git reset` ：版本回退（建议加上––hard参数，git支持无限次后悔）  
回退到上一个版本：`git reset ––hard HEAD^ ` 
回退到上上一个版本：`git reset ––hard HEAD^^`  
回退到上N个版本：`git reset ––hard HEAD~N`（N是一个整数）  
回退到任意一个版本：`git reset ––hard 版本号`（版本号用7位即可）  

`git reflog` ：查看分支引用记录（能够查看所有的版本号）  

`git rm`：删除文件（删完之后要进行commit操作，才能同步到版本库）  

`git clone`：下载远程仓库到本地  
下载远程仓库到当前路径：`git clone` 仓库的URL   
下载远程仓库到特定路径：`git clone` 仓库的URL 存放仓库的路径  

`git pull`：下载远程仓库的最新信息到本地仓库  

`git push`：将本地的仓库信息推送到远程仓库
