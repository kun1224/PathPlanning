### 指针

- 指针的本质就是地址，
- 数组也是指针，数组变量第一个元素的地址
- 传递指针给函数，会改变变量的值

### 引用

把引用作为参数，在函数内改变变量的值，变量会跟着改变

引用很容易与指针混淆，它们之间有三个主要的不同：

- 不存在空引用。引用必须连接到一块合法的内存。
- 一旦引用被初始化为一个对象，就不能被指向到另一个对象。指针可以在任何时候指向到另一个对象。
- 引用必须在创建时被初始化。指针可以在任何时间被初始化。

### 类与对象

- 成员变量声明为private，访问，修改成员变量通过函数，这就是封装

构造函数与析构函数

-  类的构造函数是一种特殊的函数，在创建一个新的对象时调用。类的析构函数也是一种特殊的函数，在删除所创建的对象时调用。

#### this指针

每个对象都有一个特殊的指针 **this**，它指向对象本身。

#### 静态成员

我们可以使用 **static** 关键字来把类成员定义为静态的。当我们声明类的成员为静态时，这意味着无论创建多少个类的对象，静态成员都只有一个副本。

### 文件和流

| 数据类型 | 描述                                                         |
| :------- | :----------------------------------------------------------- |
| ofstream | 该数据类型表示输出文件流，用于创建文件并向文件写入信息。     |
| ifstream | 该数据类型表示输入文件流，用于从文件读取信息。               |
| fstream  | 该数据类型通常表示文件流，且同时具有 ofstream 和 ifstream 两种功能，这意味着它可以创建文件，向文件写入信息，从文件读取信息。 |

### 异常处理

C++中定义的异常类：**std::exception**

#### 捕获异常

```c++
try
{
   // 保护代码
}catch( ExceptionName e1 )
{
   // catch 块
}
```

#### 抛出异常

```C++
 if( b == 0 )
   {
      throw "Division by zero condition!";
   }
```

### STL

#### 容器（Containers）

##### vector

```C++
vector<类型名> 变量名;

//迭代方式
第一种
    //v.begin()返回v的首元素地址
    vector<int>::iterator it=v.begin();
    for (int i = 0; i < v.size(); i++)
    {
       cout<<it[i]<<" ";
    }

第二种
    for (vector<int>::iterator it=v.begin(); it!=v.end();it++)
    {
        cout<<*it<<" ";
    }
第三种
    for(auto x : a)
       {
          cout<<x<<" ";
       }
```

函数

- push_back()
- pop_back()
- size()
- insert()

##### map

```C++
map<key_type, value_type>变量名

//常用方法
size()     // 计算元素个数
empty()    // 判断是否为空，空返回 true
clear()    // 清空容器
erase()    // 删除元素
find()     // 查找元素
insert()   // 插入元素
count()    // 计算指定元素出现的次数
begin()    // 返回迭代器头部
end()      // 返回迭代器尾部
    
//遍历数据
   	map<int, string>::iterator iter; //定义迭代器 iter
    for(iter = node.begin(); iter != node.end(); ++iter) {
        cout<<"身份证号"<<iter->first<<"的人叫"<<iter->second<<endl;
    }
```

#### 算法（Algorithm）

#### 迭代器（Iterators）

迭代器是指针
