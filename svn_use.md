#SVN

1. 常用命令
---
* `svn checkout`:下载服务器的代码到本地
* `svn commit`:将更改的文件提交到服务器
* `svn update`:更新服务器的代码到本地
* `svn add`:更新服务器的代码到本地
* `svn delete、svn remove `:从本地的版本控制库中删除文件
* `svn move`:移动文件或者目录或文件更名
* `svn mkdir`:创建纳入版本控制下的新目录
* `svn revert`:撤销之前的一切修改
* `svn merge`:将两个版本之间的差异合并到当前文件
* `svn info`:查看文件的详细信息
* `svn diff`:查看不同版本的区别
* `svn log`:查看日志信息
* `svn list`:列出版本库下的文件和目录列表
* `svn status`:查看文件状态
* `svn help`:获取帮助信息
* `svn lock`:加锁
* `svn unlock`:解锁

2. 检出
---
将项目检出（下载） 至本地

	svn checkout URL  [PATH]
	svn co URL  [PATH]
	
3. 提交
---
将改动过的文件提交至服务器

	svn commit  -m "注释"  [PATH]
	svn ci  -m "注释"  [PATH]
	
4. 添加
---
提交一个新建的文件到服务器，需要2个步骤  
添加新建的文件到本地的版本控制库中：`svn add`  
提交刚才的添加操作到服务器：`svn commit`  

5. 删除
---
删除服务器上的某个文件，需要做2个步骤  
将文件从本地的版本控制库中移除：`svn delete` 、`svn remove`  
提交刚才的删除操作到服务器：`svn commit`

6. 更新
---
将服务器的最新代码更新到本地

	svn update [PATH]  
	
将文件恢复至某个版本
	
	svn update -r 版本号 [PATH]