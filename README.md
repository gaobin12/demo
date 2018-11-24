# README

Hello Git

第一次练习git bash 命令

复习git上传步骤

git init 初始化

git add * 纳入缓存

git status 查看状态

git commit -m "" 纳入版本库

git remote add origin https://github.com/gaobin12/demo 建立连接

git remote -v 查看连接

git pull origin master 拉取线上的数据

在sublime中修改 

git add * 将修改后的纳入缓存

git commit -a -m "" 纳入版本库

git push -u origin master 上传

#复习git相关操作

mkdir创建目录 

ls查看当前目录

vim README.md创建readme文件并进入vim编辑器

i插入 o也是插入

git clone 地址 将远程github中的项目 克隆到本地

先按esc 然后:wq保存并退出 ：q!强制退出  要是没反应还可以esc+ZZ

cat READNE.md查看文件

cp a.txt b.txt 复制

rm a.txt移除

mv a.txt ../ 将a.txt移到上一级目录

git log查看版本修改

git config --global user.name = "" 配置用户名

git config --global user.email = "" 配置邮箱

ls -a 看看隐藏文件

# git知识

1. 查看远程仓库:
git remote -v
2. 比如 在步骤一中，我们查看到远程有一个叫origin的仓库，我们可以使用如下命令从origin远程仓库获取最新版本的代码

git fetch origin master:temp

上面代码的意思是：从远程的origin仓库的master分支下载到本地master并新建一个temp分支

注意：不建议使用pull拉取最新代码，因为pull拉取下来后会自动和本地分支合并

获取最新版本  有两种  拉取 和 获取 pull 和 fetch

git  pull     从远程拉取最新版本 到本地  自动合并 merge            git pull origin master

git  fetch   从远程获取最新版本 到本地   不会自动合并 merge    git fetch  origin master       git log  -p master ../origin/master     git merge orgin/master

实际使用中  使用git fetch 更安全    在merge之前可以看清楚 更新情况  再决定是否合并

3. 查看temp分支与本地原有分支的不同

git diff temp

4. 将temp分支和本地的master分支合并

git merge temp

现在，B的本地代码已经和远程仓库处于同一个版本了，于是B可以开心coding了。

最后再提一下，上面的步骤中我们创建了temp分支，如果想要删除temp分支，也是可以的，命令如下：

git branch -d temp

create a project

react
#git 命令

cd 切换目录

mkdir 创建目录

rm 删除

mv 移动

pwd 查看根目录

vim 启动编辑器

esc 退出 ：wq保存

git config --global --list 查看配置信息

git config --global user.name "" 配置用户名

git config --global user.email "" 配置邮箱

git上传步骤
git init

git add *

git commit -m ""

git pull --rebase origin master 这一句可以代替以下两句

git fetch

git merge

#git 从安装到与远程项目交互

下载 git

配置git用户信息 git config --global user.name "xxx" git config --global user.email "xxx"

获取密钥 ssh-keygen -t rsa -C 邮箱 一直回车

在github的settings中找到ssh配置 创建连接

测试连通性 git -T git@github.com 连接成功会在 /.ssh目录下 多一个新文件known_hosts

本地项目与远程项目关联 git remote add origin https://gaobin12/demo.git

#第一次上传（本地到远程）

git init 初始化

git add . 添加到暂存区

git commit -m "添加到本地分支 默认主分支 这里写说明"

git push -u origin master 推送到主分支

#第一次远程到本地

git clone https://gaobin12/demo.git(在github项目中复制即可)

再次提交

git add .

git commit -m "说明"

git push origin master 推送

拉取 git pull

修改文件

git add *

git commit -m ""

git push -u origin master

#取消本地目录下关联的远程库

git remote remove origin

2018/11/24
