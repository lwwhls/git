# git

### 初始化配置
    $ git config --global user.name "John Doe"
    $ git config --global user.email johndoe@example.com

1. 初始化仓库
- 初始化一个新仓库  
    git init
- 克隆一个远程仓库  
     git clone 仓库地址
      
2. 添加提交文件
- 添加文件/修改文件 提交到暂存区  
    git add file1 file2 ...
- 提交到本地仓库  
    git commit -m "提交的版本说明" 
3. 检查文件状态  
    git status  
  git status -s
  执行 git status -s ，将显示五种状态，
  
   <font color=red >??</font>   文件未加入暂存区
   <font color=green >A</font>   新增加的文件加入到暂存区
   <font color=red >M</font>   修改已存在的文件，但未加入暂存区 
   <font color=green >M</font>  修改已存在的文件,并且加入暂存区 
   <font color=green >M</font> <font color=red >M</font> 再次修改已提交到暂存区的文件 
  
    
4. 输出工作区和暂存区的different(不同)。
git diff
5. 查看提交历史
git log
6. 修改删除文件
- 删除文件
git rm file

```
rm -f file
git add file
```
- 移动重命名文件
git mv fileA fileB
- 撤消还原操作
取消暂存文件 git reset HEAD file
还原本地文件 git checkout -- file
恢复工作目录（取消所有操作） git reset --hard

7. 远程仓库
- 添加远程仓库
- 删除远程仓库
- 重命名远程仓库
- 更新推送远程仓库
- 设置获取仓库地址
8. 分支管理
- 创建分支
- 切换分支
- 合并分支
- 删除分支
- 移动或重命名分支
- 复制分支

9.忽略文件设置
 - 创建文件
 
 在git管理的项目文件夹中（严格的讲，应该叫做git的本地repository），创建一个文件名为“.gitignore”的纯文本文件；
 
 - 编辑文件
 
编辑.gitignore文件，以下编辑时是常用的规则：

1）/mtk/               过滤整个文件夹

2）*.zip                过滤所有.zip文件

3）/mtk/do.c         过滤某个具体文件

很简单吧，被过滤掉的文件就不会出现在git仓库中（gitlab或github）了，当然本地库中还有，只是push的时候不会上传。需要注意的是，gitignore还可以指定要将哪些文件添加到版本管理中：

1）!*.zip

2）!/mtk/one.txt

.gitignore配置文件用于配置不需要加入版本管理的文件，配置好该文件可以为版本管理带来很大的便利，以下是对于配置.gitignore的一些心得记录：

以斜杠“/”开头表示目录；

以星号“*”通配多个字符；

以问号“?”通配单个字符

以方括号“[]”包含单个字符的匹配列表；

以叹号“!”表示不忽略(跟踪)匹配到的文件或目录；

- Tips

1.）git 对于 .ignore 配置文件是按行从上到下进行规则匹配的，意味着如果前面的规则匹配的范围更大，则后面的规则将不会生效；

2.）如果.gitignore忽略规则创建于文件提交代码库之后，则.gitignore规则不会影响目前所提交的文件（不会自动把文件从服务器端删除掉）。你需要手动删除已被追踪的文件；

删除被追踪的文件：git  rm --cached filename（文件名称）

删除被追踪的文件夹：git  rm --cached -r foldername（文件夹名称）




