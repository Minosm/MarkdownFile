commit 就是快照

repo（repository的缩写）

staging area（暂存区）又叫index

branch拥有创建时那个节点的所有信息。

###### 两个指针

- ###### branch指针（指向commit）  

- ###### head指针（指向branch）——symbolic pointer（符号指针）



decor, 装饰——decorate（德克士？ ）



##### 两层指针

- ###### 一层是指向当前commit的branch指针

- ##### 另一层是指向branch的head指针————checkout语句控制着这一指针

###### 每一次commit本质是指针移动的过程



git branch --merged

git log 好多参数

#### alias（别名）



###### 强制删除是-D

因为有些merge并未完成的branch，无法直接用-d删除，所以要用-D



###### merge 是基于commit 的 merge



git merge -abort（反悔）流产

###### merge 结束后应继续 commit（保存快照）



##### detached HEAD（特殊warning状态）

可以使用git checkout hashvalue，让head指向某个commit，而不是branch

（checkout一般只用于branch）

> You are in 'detached HEAD' state. You can look around, make experimental(实验性的)
> changes and commit them, and you can discard（丢失） any commits you make in this
> state without impacting（影响） any branches by switching back to a branch.
>
> If you want to create a new branch to retain commits you create, you may
> do so (now or later) by using -c with the switch command. Example:
>
>   git switch -c <new-branch-name>
>
> Or undo this operation with:
>
>   git switch -
>
> Turn off this advice by setting config variable advice.detachedHead to false（还可以关闭该状态）——手法？
>
> HEAD is now at 4172220 v2

此时查看状态会告知你这一分离状态



##### git stash

可以快速保存，剩下add和commit的功夫

> ###### git stash save "text" 
>
> 在stash的时候顺便载入提示信息，防止忘记某个存档点的内容

###### git stash list [-p]

###### git stash list apply——直接恢复最近一次的删除（stash仍在）

git diff 查看不同

git pop（从栈中弹出，stash不存在了）

###### git stash apply label(前面的复制下来)，可以恢复任意stash记录



三向merge，会新增commit点进行merge



alias graph='git log --all --decorate --oneline --graph'



