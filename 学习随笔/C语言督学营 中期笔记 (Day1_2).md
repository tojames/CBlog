﻿@[toc]
# 中期第1次直播  typedef  
## typedef
定义方法：

```c
typedf  struct student {
   int num ;
   char name[20] ;
   char sex ;
}  stu , * pstu ;
```

- `stu`    代表  `struct student` （给结构体类型起别名）
 - `* pstu`  代表 `struct studen  *`  （给结构体指针变量起别名）

- `typedef  int INTEGER`    起别名的作用在于**代码即注释**


## C++ ‘&’  符的运用
-  把`&`写到形参的位置是C++的语法，称为引用
```cpp
#include  <stdio.h>

void modify_num(int &b){
   b = b+1 ;
} 

int main(){
  int a = 10 ;
  modify_num(a) ;
  printf("a=%d\n",a) ;
  return 0 ;
}
```
 - 如果将 引用改为纯C 的写法如下：
![在这里插入图片描述](https://img-blog.csdnimg.cn/3949d9ad0d1147e6841ada7aaa77142a.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBAUXVhbnR1bVlvdQ==,size_15,color_FFFFFF,t_70,g_se,x_16)
**运用引用操作指针**
![在这里插入图片描述](https://img-blog.csdnimg.cn/4991b73455ac435c80a49c1033e019cf.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBAUXVhbnR1bVlvdQ==,size_20,color_FFFFFF,t_70,g_se,x_16)
# 中期第2次直播   逻辑/物理 结构

**逻辑结构**：集合结构、线性结构、树形结构、图形结构

**物理结构**：顺序存储、链式存储、索引存储、散列存储

<font color=red>顺序存储与随机存储对比</font>

![在这里插入图片描述](https://img-blog.csdnimg.cn/154fb154528648a4b227e8dd8b1240d3.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBAUXVhbnR1bVlvdQ==,size_20,color_FFFFFF,t_70,g_se,x_16)

## 时间复杂度、空间复杂度

- 时间复杂度指算法中所有语句的频度（执行次数）之和。
- 空间复杂度指算法运行过程中所使用的辅助空间的大小。

## 线性表的顺序存储及其原理实现

![在这里插入图片描述](https://img-blog.csdnimg.cn/e1907c9ebb2d4400a122deb23425cd27.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBAUXVhbnR1bVlvdQ==,size_20,color_FFFFFF,t_70,g_se,x_16)

> 注意： 动态分配的数组还还是**属于**顺序存储结构，动态分配并不是链式存储，同样是顺序存储，其物理结构没有发送变化，依然是随机存取方式，只是分配的空间大小可以在运行时决定。

动态分配形式   `int * p = (int *)malloc(size of(int)*10)`


![在这里插入图片描述](https://img-blog.csdnimg.cn/ca124f8ffb724c0bad464bcc1dfaafe5.png)

> 有序： 不一定是按从小到大或从大到小





