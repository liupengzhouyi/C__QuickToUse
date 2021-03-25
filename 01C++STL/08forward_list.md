# C++ forward_list

## 这是什么？

* 单向链表。
* 只支持单向顺序访问。
* 在链表的任何位置进行插入、删除操作都很快。

## 头文件

```c++
#include <forward_list>
```

## 创建 forward_list 容器

* 创建一个没有任何元素的空 forward_list 容器：

```c++
std::forward_list<int> values;
```

* 创建一个包含 n 个元素的 forward_list 容器：

```c++
// 每个元素的值都为相应类型的默认值（int类型的默认值为 0）。
std::forward_list<int> values(10);
```

* 创建一个包含 n 个元素的 forward_list 容器，并为每个元素指定初始值。例如：

```c++
std::forward_list<int> values(10, 5);。
```

* 在已有 forward_list 容器的情况下，通过拷贝该容器可以创建新的 forward_list 容器。

```c++
// 必须保证新旧容器存储的元素类型一致。
std::forward_list<int> value1(10);
std::forward_list<int> value2(value1);
```

* 通过拷贝其他类型容器（或者普通数组）中指定区域内的元素，可以创建新的 forward_list 容器。例如：

```c++
//拷贝普通数组，创建forward_list容器int 
a[] = { 1,2,3,4,5 };
std::forward_list<int> values(a, a+5);

//拷贝其它类型的容器，创建forward_list容器
std::array<int, 5>arr{ 11,12,13,14,15 };
std::forward_list<int> values(arr.begin()+2, arr.end());//拷贝arr容器中的{13,14,15}
```



## 添加&删除

```c++
fl.push_front()				// 在容器头部插入一个元素。
fl.pop_front()					// 删除容器头部的一个元素。
```

## 排序

```c++
fl.sort();
```

