##### 代码仓库之一

最有名，最知名，最牛逼

gitlab 代表性——是开源软件，帮助自己搭建代码托管平台（大公司）

小公司都是GitHub。

###### GitHub推送语法：

~~~
git remote add mercury https://github.com/Minosm/GitStudy.git
~~~

> 把mercury设为云端的别名，即“句柄”

~~~
git push [-u] mercury master
~~~

> 推送branch，云端保存
>
> ###### 这里-u 是指定mercury为默认推送 
>
> ###### 下一次直接push即可推送该次设置的值



~~~
git branch -M main
~~~

> git branch -M main 重命名为main

图书馆的垃圾网让我不得不选择之后在宿舍继续学习GitHub，	P14

MARK一下；

终于把那两条笨蛋分支推上去了，现在开始学怎么拉下来。

##### git clone  mercury(地址)

###### 原来，绿色code那里的clone，是配合着git使用的！

git clone address即可

要等一会儿，成功之后可以在clone的文件夹下找到自己的repository 目录

进入该目录，即可对代码进行操作。

> git brach 的时候，除了main分支外的其他分支并不会显示，但存在。
>
> 可以通过且换分支告知git，其他分支的存在。

##### 建议把统一资源定位符的别名改为origin

因为系统默认就是这个。。。（在其他终端clone一次后，默认会把url的别名设置为origin）

##### pwd可以查看自己位置——print work dictionary

##### ls是查看文件夹内容

##### touch 是新建文件





