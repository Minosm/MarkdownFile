什么是[EJB](https://blog.csdn.net/kouzhaokui/article/details/89176541)?

什么是[POJO](https://baike.baidu.com/item/POJO)?

[网课地址](https://www.icourse163.org/spoc/learn/JUST-1450258162?tid=1450671443#/learn/content?type=detail&id=1216124923&cid=1221440358&replay=true)

什么是[TOMCAT](https://www.leiue.com/what-is-tomcat)?

- 先把JSP编译成serverlet

- TOMCAT是JSP引擎，他调用Java编译器把serverlet文件编译成可执行的字节码文件

- 应用服务器

  - > 严格意义上Web服务器只负责处理HTTP协议，只能发送静态页面的内容。而JSP，ASP，PHP等动态内容需要通过CGI、FastCGI、ISAPI等接口交给其他程序去处理。这个其他程序就是应用服务器。
    >
    > 　　（1）Web服务器的设计目的是提供HTTP内容，应用服务器也可以提供HTTP内容，但不限于HTTP，它还可以提供其他协议支持，如RMI / RPC。
    >
    > 　　（2）Web服务器主要是为提供静态内容而设计的，不过大多数Web服务器都有插件来支持脚本语言，比如Perl、PHP、ASP、JSP等，通过这些插件，这些服务器就可以生成动态的HTTP内容。
    >
    > 　　（3）大多数应用服务器都将Web服务器作为其不可分割的一部分，这意味着应用服务器可以做任何Web服务器所能做的事情。此外，应用服务器有组件和特性来支持应用级服务，如连接池、对象池、事务支持、消息传递服务等。
    >
    > 　　（4）由于web服务器非常适合用于提供静态内容，而应用服务器适合提供动态内容，因此大多数生产环境都有web服务器充当应用服务器的反向代理。这意味着在页面请求时，web服务器会通过提供静态内容(例如图像/静态HTML)来解释请求，并且它还会使用某种过滤技术(主要是请求资源的扩展)识别动态内容请求，并透明地转发到应用服务器。

什么是JAVABEAN?

- 数据的管理？
- 组件？

WEB sever

- HTTP sever
- APPLICATION server
  - Serverlet Container
  - CGI Sever
  - ……

<img src="C:\Users\Minos Chen\AppData\Roaming\Typora\typora-user-images\image-20200530091542838.png" alt="image-20200530091542838" style="zoom:50%;" />

tomcat是服务器的web支持软件；

TOMCAT的正确理解：

- > ![image-20200530104555192](C:\Users\Minos Chen\AppData\Roaming\Typora\typora-user-images\image-20200530104555192.png)

本质是软件，是用于解析JSP文件的引擎，也可以叫做JSP容器，只有当服务器安装了TOMCAT之后，才可以将它们称为“Web服务器”！！！

> 安装了JSP引擎的计算机就是Web服务器

> Web服务器仅仅提供了一个可以执行服务器端程序和返回程序所产生的影响的一个环境，而不会超出它的职责
>
> Web服务器主要是处理向浏览器发HTTP的请求以供客户端浏览器网页。

> 当一台机器上配置好Apache服务器，可以利用它响应对HTML页面的请求。
>
> 实际上Tomcat部分是Apache服务器的扩展，但是可以它是可以独立运行的，所以当你运行一个tomcat的时候，它实际上作为一个与Apache独立的进程单独运行的能力；
>
> Tomcat则既能为静态网页提供服务，同时也能够为动态网页提供服务支持（因为它包含JSP容器和Servlet容器也可以称之为JSP引擎），尽管Tomcat的速度和功能没有Web服务器快和多，但是Tomcat也逐渐为支持静态的内容不断扩大，大多数的Web服务器都是由C语言等，利用了相应平台的特征，因此用纯Java编写的Tomcat速度上是肯定会稍稍逊色的

> JRun：
>
> JRun是一个JSP引擎，与Tomca一样用来管理和运行Web应用程序（收费的）
>
> Resin：
>
> Resin是一个JSP引擎，用来管理和运行一个Web程序，是CAUCHO公司开发的Java服务器端的软件，Resin运行JSP的速度非常的快速而且是不收费的！！