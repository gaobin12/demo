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
