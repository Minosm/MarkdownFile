#### 又是python写的

高级扫描，定制数据包

scapy

伪装报文

##### 定制arp协议：ARP().display()

hwtype = 0x800 硬件类型

ptype= 0x800  协议类型	 

hwlen= 6	 硬件地址长度(MAC) 

plen= 4 协议地址长度(IP) protocol

op= who-has who-has查询	 

hwsrc= 00:0c:29:6a:cf:1d   源MAC地址	 

psrc= 192.168.1.53	源IP地址	 source

hwdst= 00:00:00:00:00:00  hardware

pdst= 0.0.0.0  向谁发送查询请求 destination ip

---

sr1 函数，发送与接收数据包；

##### sr1(ARP(pdst="192.168.1.1"))

> IP().display()
> ###[ IP ]### 
> version= 4	版本
> ihl= None	首部长度 IP head length
> tos= 0x0 服务（type of service）
> len= None 总长
> id= 1	标识
> flags= 
> frag= 0	标志
> ttl= 64	生存时间 （time to live）
> proto= hopopt	传输控制协议 IPV6逐跳选项
> chksum= None 首部校验和  check sum
> src= 127.0.0.1 源IP
> dst= 127.0.0.1 目的IP

##### ICMP

> | type= echo-request  类型,标识ICMP报文的类型 |
> | ------------------------------------------- |
> | code=0 代码                                 |
> | chksum= None 校验和                         |
> | id= 0x0  标识                               |
> | seq= 0x0                                    |

#### ping命令需要组合使用ICMP和IP命令，生成ping包进行探测

IP（）生成源IP和目标IP

ICMP（）生成 ping包的**类型** 

sr1是发送、接收数据包



#### 定制TCP协议的SYN请求

| 2      | **sport= ftp_data TCP源端口 source port**                    |
| ------ | ------------------------------------------------------------ |
| 3      | **dport= http destination port TCP目的端口**                 |
| 5      | seq= 0 32位序号                                              |
| 7      | ack= 0 32位确认序号                                          |
| 9      | dataofs= None T 4位首部长度                                  |
| 10     | reserved= 0 保留6位                                          |
| 12     | **flags= S 标志域   紧急标志、有意义的应答标志、推、重置连接标志、同步序列号标志、** |
| **14** | **完成发送数据标志。按照顺序排列是: URG, ACK, PSH, RST, SYN, FIN** |
| 15     | window= 8192 窗口大小                                        |
| 16     | chksum= None 16位校验和                                      |
| 17     | urgptr= 0 优先指针  urgent pointer                           |
| 18     | 优先指针                                                     |
| 19     | options=[] 选项                                              |

我刚刚自定义了快捷键！！！

> ### CTRL + SHIFT + D 删除所在行
>
> ### SHIFT + ALT + D 删除所在列

配合有道的OCR 无敌！！！



##### **URG和PSH**的区别

URG（紧急数据标志位）：如果URG为1，表示本数据包中包含紧急数据。此时紧急数据指针表示的值有效，它表示在紧急数据之后的第一个字节的偏移值（即紧急数据的总长度）。若URG为0，则紧急指针没有意义。

PSH（推位）：当设置为1时，要求把数据尽快的交给应用层，不做处理。
当两个应用进程进行交互式的通信时，有时在一端的应用进程希望再键入一个命令后立即就能够收到对方的响应。在这种情况下，TCP就可以使用推送操作。这时，发送方TCP把PSH置1，并立即创建一个报文段发送出去。接收方TCP收到PSH=1的报文段，就尽快交付接收应用进程，而不再等到整个缓存都填满了再向上交付。
虽然应用进程可以选择推送操作，但推送操作还是很少使用。

两者都可理解为处理紧急数据的标志位，只是处理方法不同。URG的紧急数据仅在报文内，而PSH的紧急数据还在接受缓冲区内。

#### sr1(IP(dst="192.168.1.1")/TCP(flags="S" ,dport=80),timeout=1)

s就是syn的简称

flags=SA 意思是flag有两个，syn和ack

- 可以看出是第二次握手了已经
- 因为没有第三次握手，所以是半连接
  - 更隐秘！
- 