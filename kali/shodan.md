##### 工作原理

~~~
Shodan每隔一段时间就会对全球大约8亿主机进行扫描，通过对返回Banner信息的处理，识别特定主机，并进行分类储存。为了避免因政治、技术等原因导致的扫描信息误差（比如某墙或某些老美服务商对大陆羊毛党的屏蔽等），Shodan的扫描主机至少遍布在全球的8个国家和地区。
~~~

###### HTTP banner

~~~
Shodan的Banner处理机制比较复杂，我们这里只需要知道探测端口是来往的数据包中包含Banner，并包含了主机的部分信息即可
~~~

### 基本查询

~~~bash
hostname："主机或域名"   如 hostname:"google''
port："端口或服务" 如 port:"80"
ip : "ip地址" 如 ip : "114.114.114.114"
net："IP地址或子网"如 net:"111.112.113.110.0/24"
vuln :指定漏洞的cve如 vuln:CVE-2015-8869
但是这个命令最好搭配起来使用，如 country:CN vuln:CVE-2018-0610
os :"操作系统" 如 os:"debian"
isp："ISP供应商" 如 isp:"China Telecom"
product："操作系统/软件/平台" 如 product:"nginx"
version："软件版本" 如 version:"1.16.0"
geo："经纬度" 如 geo:"38°53.707′,77°02.182"
country`："国家" 如 country:"China"
city："城市"  如 city:"shanghai"
org："组织或公司" 如org:"google"
before/after："日/月/年" 如 before:"11/05/2019" after:"11/05/2019"
asn : "自治系统号码" 如 asn:"TS1826"
~~~

##### 关联查询

~~~bash
Apache city:"shanghai" port:"8080"
~~~

https://www.jianshu.com/p/f65075fc1b4c

还有很多付费功能。

 exploits（漏洞）

> shodan是美国开发的，号称是最邪恶的搜索引擎，国内也开发了类似的一个叫Fofa。shodan和Fofa都是一种基于网络资产发现的搜索引擎，他会爬取全网中的设备探测他开放的端口，将探测到的banner信息存储。从安全角度来说，利用这种搜索引擎可以进行资产及漏洞影响范围分析、应用分布统计、应用流行度态势感知等。从不合理的角度来说，利用这种搜索引擎可以发现哪些设备开放了不安全的端口或者服务，可以轻松的进入一些监控设备、工业控制设备、项目后台等





##### 百度黑客？？？

> inurl:/admin/login.php