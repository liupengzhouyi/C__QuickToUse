# C++ Map

* 这是一个key-value类型列表的结构

* 大致就是这样，然后开始介绍这个数据结构应该如何使用

## 头文件

```c++
#include <map>
```

## 声明&初始化

```c++
std::map<std::string, int> mapPerson;
```

## show me you size

```c++
my_Map.size()           //返回元素数目 
my_Map.empty()          //判断是否为空 
my_Map.clear()          //清空所有元素 
```

## 修改

```c++
//插入数据
my_Map["a"]；        //只插入键，对应的值默认为0
my_Map["a"] = 1;    //同时插入键和值

my_Map.insert(map<string,int>::value_type("b",2)); 
my_Map.insert(pair<string,int>("c",3)); 
my_Map.insert(make_pair<string,int>("d",4)); 
```

## 删除数据
```c++
my_Map.erase(my_Itr); 
my_Map::iterator my_Itr; 

my_Map.erase("c"); 
```

## 访问(查找)元素

### Way No.1:

```c++
int i = my_Map["a"]; 
```

### Way No.2

```c++
MY_MAP::iterator my_Itr; 
my_Itr = my_Map.find("b"); 
if (my_Itr != my_Map.end())
{
	int j = my_Itr->second;       //first返回键，second返回值
}
```

## 遍历

### 前向迭代器

```c++
	std::map<std::string, int>::iterator it;
  std::map<std::string, int>::iterator itEnd;
  it = mapPerson.begin();
  itEnd = mapPerson.end();
  while (it != itEnd) {
		cout<<it->first<<' '<<it->second<<endl;  
    it++;
  }
```

### 反向迭代器

```c++
std::map<std::string, int>::reverse_iterator iter; 
for(iter = mapPerson.rbegin(); iter != mapPerson.rend(); iter++)
{
	std::cout << iter->first << "  " << iter->second << std::endl; 
}
	
```

