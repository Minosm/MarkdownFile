### **形态学函数（MorphologyEx）**

高级形态学变换，本质也是腐蚀和膨胀；

使用**morphologyEx**函数调用：

###### 五种：

###### **1. 开运算（Opening Operation） = 先腐蚀，后膨胀**

dst=open(src,element)=dilate(erode(src,element))



**2. 闭运算（Closing Operation） = 先膨胀，后腐蚀**

dst=close(src,element)=erode(dilate(src,element))



**3. 形态学梯度（MorphologicalGradient） = 膨胀图 - 腐蚀图胀**

dst=morph_grad(src,element)=dilate(src,element)?erode(src,element)

​	

**4. 顶帽（Top Hat） = 原图 - 开运算图**

dst=tophat(src,element)=src?open(src,element)



**5. 黑帽（Black Hat） = 闭运算图 - 原图**

dst=blackhat(src,element)=close(src,element)?src

https://blog.csdn.net/poem_qianmo/category_1923021.html

