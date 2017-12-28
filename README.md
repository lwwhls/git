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

