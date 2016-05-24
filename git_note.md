###Git Learning Note

#####初始化
- 创建版本库
	- git init

#####git的增删改查
- 增加
	- git add <fileName> 
- 删除
	- git rm <fileName> (-r <dirName>)
- 撤销修改
	- git checkout -- <fileName> 
- 修改（提交）
	- git commit -m "message"
- 查看（当前状态信息）
	- git status

	
#####分支操作
- 创建分支
	- git branch <branchId>
- 切换分支
	- git checkout <branchId>
- 创建并切换分支
	- git checkout -b <branchId> 
- 合并分支
	- git merge <branchId> (将<branchId>合并到当前分支)
- 删除分支
	- git branch -d <branchId>
- 版本回退(前进)
	- git reset --hard <commit id>(也可以用HEAD标示当前版本。上一个版本就是HEAD^，上上一个版本就是HEAD^^，当然往上100个版本写100个^比较容易数不过来，所以写成HEAD~100。)
	
#####bug分支

#####冲突解决

#####远程仓库

#####git自定义

#####其它常用命令
- 查看git日志
	- git log（用于查看commit信息列表） 
- 查看命令历史
	- git reflog
	
#####参考文献
[廖雪峰Git教程](http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000)