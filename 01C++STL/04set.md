# C++ Set

## 大致了解一下

> * set跟vector差不多,
> * 它跟vector的唯一区别就是，set里面的元素是有序的且唯一的，
> * 只要你往set里添加元素，它就会自动排序
> * 如果你添加的元素set里面本来就存在，那么这次添加操作就不执行。
> * 要想用set先加个头文件set。

## 头文件

```c++
#include <set>
```



## 案例

###  初始化

```c++
set<int> s;
```

### 插入元素

```c++
s.insert(1);
s.insert(3);
s.insert(5);
```

### 查找元素

```c++
set<int>::iterator it;
it = s.find(1);
if(it==s.end()) 
{
	puts("not found");
}
else 
{
	puts("found");
}
```

### 删除元素

```c++
s.erase(3);
```

### 遍历所有元素

```c++
set<int>::iterator it;
for(it=s.begin();it!=s.end();it++){
        printf("%d\n",*it);
}
```

