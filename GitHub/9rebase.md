###### rebase（变基）

使git记录变得简洁，把多个记录整合成一个。

stash？？存放，和commit差不多；

VIM:

> 退出命令是，按`ESC`键 跳到命令模式，然后输入`:q`（不保存）或者`:wq`（保存） 退出。
>

合并没有提交过的版本

commit前应该尝试着rebase，把可以合并的记录都给合并了。

- 多条记录合并为一条（线性）

- 去掉分支记录
- pull 的时候，会有merge，为了避免merge 导致的分支，可以拆分pull，用rebase代替merge

#### 连续写的时候可以加 \ 来继续

查看commit记录图表的时候，可以用

> git log --graph 

简洁版：

> git log --graph --pretty=format:"%h %s"

h 是哈希值，即commit事件的（版本），s是记录（名称）

###### rebase 的时候会产生冲突，然后解决冲突，(先add)git rebase --continue

vim 1.py



#### 面试经常考！！！