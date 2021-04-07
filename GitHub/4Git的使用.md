###### git 是一种版本库文件格式

分布式版本控制软件

版本控制的四个步骤：

- 进入文件夹——git bash here
- 初始化（提权）git init
- 增删改查
- 生成版本

git init 初始化

git status 检测文件状态

git add 管理 + 文件名/"."_全部

git commit -m 'version name' 生成版本了

> 如果未add ，则无法直接使用commit

git log 查看版本记录

###### git三大空间

[Git.xmind](..\..\X-mind_files\其他\Git.xmind) 



![git](D:\File_Recv\日语学习\git.jpg)



版本控制的好处是可以快速回滚到之前的版本：

回滚：

- git reset --hard commit后的**版本号**

### reset 的本质：移动 HEAD 以及它所指向的 branch

- > head 是头指针
  >
  > 如果直接reset，**并不会改变文件！！！** 好像是只操作了暂存区

普通的git log无法查看已删除

需用git reflog（reset flow log）查看所有和commit记录

vi 查看文件 

ZZ 退出（大写）

cat concatenate (使链接)

reset **--hard** 会清空工作目录和暂存区的改动，而 **--soft则会保留工作目录的内容，并把因为保留工作目录内容所带来的新的文件差异放进暂存区**。

reset 不加参数(mixed)：保留工作目录，并清空暂存区

**reset** 如果不加参数，那么默认使用 **--mixed** 参数。它的行为是：保留工作目录，并且清空暂存区。也就是说，工作目录的修改、暂存区的内容以及由 **reset** 所导致的新的文件差异，都会被放进工作目录。简而言之，就是「把所有差异都混合（mixed）放在工作目录中」。







