zhangxy,welcome to git

######安装完后，打开git.bash配置用户和邮箱

git config --global user.name "zhangxy"
git config --global user.email "email@example.com"

######install repository:安装仓库：
cd /
cd f
mkdir zxy_git #创建zxy_git目录
cd zxy_git
pwd #显示当前路径
git init #把当前目录变成repository

###### 注意，不要用记事本打开文件，用notepad++，编码调成utf8 without BOM格式

###### 在zxy_git目录下新建个readme.txt文本，提交到git：
######第一步，用命令git add告诉Git，把文件添加到仓库：（可以add多个再一起提交）
git add readme.txt
git add helloworld.txt
第二步，用命令git commit告诉Git，把文件提交到仓库：（-m后面的是提交说明）
git commit -m "添加了readme.txt和helloworld.txt两个文件"

git status #查看当前仓库状态
git diff readme.txt #查看readme.txt的修改
######git add 和 git commit提交修改（和提交新文件一样，当时git commit之前建议先git status一下）

git reset --hard commit_id 回到某个版本id的版本; 
git reset --hard HEAD^ 回到当前版本的前一版本（两个^为前两个版本,以此类推）;

git log 查看提交历史
git log --pretty=oneline 简化查看提交历史
git reflog 查看命令历史,可以回到被覆盖的新版本

######实际上git add只是把内容从工作间放在暂存区，git commit才是把内容提交到分支（默认master）（暂存区也在版本库里）
######git add 之后又修改了，git commit只会提交第一次修改（git add之前的修改），因为第二次的修改没在暂存区，在工作间

git diff HEAD --readme.txt 查看本地readme.txt和master分支当前版本是否一样

