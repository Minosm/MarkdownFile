le,novo  /,li'nəuvəu/

###### net user 

add/del

- add

  - net user admin pwd /add

- ###### delete(del)

  - net user admin /del

- 查看用户信息
  - net user admin

##### 提权

用户组操作

- 把自己新建用户放到管理员用户组里

  > net localgroup administrators admin /add

  在net 主操作里，使用localgroup副操作，在administrators组内添加admin用户

  > 为啥我提权火绒都不管的?

- 把用户组中的用户删除

  > net localgroup users admin /del

  在……，users组中删除admin用户