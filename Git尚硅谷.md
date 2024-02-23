# [Git](https://git-scm.com/)
## 分布式**版本控制**工具 VS 集中式**版本控制**工具
版本控制:
  - 版本控制是一种<u>记录文件内容变化</u>，以便将来查阅特定版本修订情况的系统
  - 版本控制其实最重要的是可以<u>记录文件修改历史记录</u>，从而让用户能够查看历史版本，方便版本切换
  - （班长就是Git）

版本控制工具:
 - 集中式版本控制工具：多个客户端统一从中央服务器里控制代码
 - 分布式版本控制工具：本地库 远程库

工作机制:
 - 远程库：Github，码云等基于网络服务器的远程代码仓库
 - 通常 要从本地库 push 到远程库![[Pasted image 20240222215015.png]]
## Git命令 基于开发案例 常用命令

git config --global user.name 用户名    设置用户签名
git config --global user.name 邮箱        设置用户签名

### 基本语法
1. git init （初始化本地库）
先找到你要初始化的本地库，右键打开git bash并运行git init

2. git status (查看状态) 

3. git add  \<filename> （将文件添加到暂存区）

4. git rm --cashed \<filename>（删除暂存区里的文件）

5. git commii -m '日志信息' \<filename> （提交本地库）

6. git reflog/git log （查看提交信息 历史版本）

### 版本穿越
通过 git reflog 找到你要穿越的版本号
再使用 git reset --hard \<版本号> 穿越回该版本

## Git分支 分支特性 分支创建 分支转换 分支合并 代码合并冲突解决
分支操作:
1. git branch -v （查看分支）
2. git branch \<branchname> （创建分支）
3. git checkout \<branchname> （切换分支）
4. git merge \<branchname> （合并分支）
5. git在冲突合并中不会自动合并，因此要手动打开文件进行修改，然后把修改好的文件git add和git commit （注意：git commit 后不需要加文件名）
## IDEA 集成Git
# [Github](http://github.com)
## 远程仓库操作
1. 在github上创建远程仓库
2. 远程仓库操作
	- git remote -v 查看当前远程仓库别名
	- git remote add \<别名> \<远程仓库链接> 创建远程仓库别名（因为github的远程库的链接太长，我们为其创建一个简短的别名）
3. push 将本地库上传到远程库
	git push \<别名> \<branchname> 本地库推送到远程库的单位是分支（branch） 该操作就是将本地库中的文件发送到远程库
4. pull 将远程库拉取到本地库
	git pull \<别名> \<branchname>
5. clone 将远程库克隆到本地
	git clone \<库链接> 在某文件夹下git bush该命令行会将目标库直接克隆
	git clone 将会做以下操作：拉取代码 初始化本地仓库 创建别名
6. pull request 提交修改
	 首先将github上的库fork到自己账号中
	 然后再自己账号中修改要修改的东西，提交修改（此时仅仅修改了自己账号中的库）
	 点击Pull request，new pull request，create pull request
## IDEA 使用Github
# Gitee 码云
## 码云创建远程库
## IDEA集成码云
## 码云连接Github进行代码复制和迁移
# Gitlab
## Gitlab服务器搭建和部署
## IDEA集成Gitlab