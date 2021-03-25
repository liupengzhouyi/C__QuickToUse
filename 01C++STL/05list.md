# C++ List 

## 这是什么？

* 双向链表。
* 只支持**双向顺序访问**。
* 在list中任何位置进行插入、删除操作速度都很快。
* 适用于少量读写，大量插入，删除的情况。

## 头文件

```c++
#include <list>
```

## 声明&初始化

```c++
 list<int> l;
```

## show me you size

```c++
l.empty() 		// 判空
```

## 元素访问



```c++
    l.front();                       // 取队头元素
    l.back();                        // 取队尾元素
```

## 修改

```c++
  l.push_back();                        // 尾后压入元素
  l.push_front();                       // 队头压入元素
  
  l.pop_back();                         // 尾后弹出一个元素
  l.pop_front();                        // 队头弹出一个元素
  
  l.insert(l.begin(), 88);              // 某个位置插入元素(性能好)
  
  l.remove(2);                          // 删除某个元素(和所给值相同的都删除)
  l.erase(--l.end());                   // 删除某个位置的元素(性能好)
```

## 遍历

```c++
list<int>::iterator it;  

for(it = l.begin(); it!=l.end(); it++)   
{
   cout<<*it<<endl;
}
```

## 排序

```c++
l.sort();           //注意与vector的排序使用方法不一样
```



## 翻转

```c++
l.reverse();                                // 倒置所有元素
```

