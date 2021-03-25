# C++ Vector

我知道有这么一个东西，用的不熟练，

妈的，VS code 还没有自动补全，他的方法我会没有用熟练。这个难搞！

## 使用必备头文件

```c++
#include <vector>
```

## 初始化

```c++
vector<int> vec;        //声明一个int型向量
vector<int> vec(5);     //声明一个初始大小为5的int向量
vector<int> vec(10, 1); //声明一个初始大小为10且值都是1的向量
vector<int> vec(tmp);   //声明并用tmp向量初始化vec向量
```

## 容量

```c++
vec.size();            //大小
vec.capacity();        //真实大小
vec.max_size();        //最大容量
vec.resize();          //更改大小
vec.empty();           //判空
```

## 修改

```c++
vec.push_back();        							//末尾添加元素
vec.insert(vec.begin()+i,a); 					// 在第i+1个元素前面插入a;

vec.pop_back();      	  							//末尾删除元素
vec.erase(vec.begin()+2); 						//删除第3个元素
vec.erase(vec.begin()+i,vec.end()+j); //删除区间[ i,j-1] 区间从0开始

vec.swap();          	  							//交换两个元素
vec.clear();            							//清空元素
```

## 元素的访问

```c++
vec[1];       //下标访问,并不会检查是否越界
vec.at(1);     //at方法访问,以上两者的区别就是at会检查是否越界

vec.front();     //访问第一个元素
vec.back();      //访问最后一个元素 

int* p = vec.data();    //返回一个指针,可行的原因在于vector在内存中就是一个连续存储的数组，所以可以返回一个指针指向这个数组。这是是C++11的特性。
```

## 遍历

```c++
vector<int>::iterator it;
for (it = vec.begin(); it != vec.end(); it++)
    cout << *it << endl;
//或者
for (size_t i = 0; i < vec.size(); i++) {
    cout << vec.at(i) << endl;
}
```

## 排序

```c++
#include<algorithm>
sort(vec.begin(), vec.end()); //采用的是从小到大的排序

bool Comp(const int& a, const int& b) {
    return a > b;
}
sort(vec.begin(), vec.end(), Comp);
```

## 翻转

```c++
#include <algorithm>
reverse(vec.begin(), vec.end());
```

先就是这些，用到在说！

