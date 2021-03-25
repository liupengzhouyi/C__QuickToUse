# C++ Pair

* pair是将2个数据组合成一组数据



## **pair的创建和初始化**

* 创建空对象

```c++
pair<string, string> anon;        // 创建一个空对象anon，两个元素类型都是string
pair<string, int> word_count;     // 创建一个空对象 word_count, 两个元素类型分别是string和int类型
pair<string, vector<int> > line;  // 创建一个空对象line，两个元素类型分别是string和vector类型
```

* 当场初始化

```c++
pair<string, string> author("James","Joy");    // 创建一个author对象，两个元素类型分别为string类型，并默认初始值为James和Joy。
pair<string, int> name_age("Tom", 18);
pair<string, int> name_age2(name_age);    // 拷贝构造初始化
```

* 赋值

```c++
pair<int, string> newone;
newone = make_pair(a, m);
```



## 访问

```
pair<int ,double> p1;
 
p1.first = 1;
 
p1.second = 2.5;
 
cout<<p1.first<<' '<<p1.second<<endl;
 
//输出结果：1 2.5
 
 
string firstBook;
if(author.first=="James" && author.second=="Joy")
    firstBook="Stephen Hero";
```

