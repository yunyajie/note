* 一.变量
    * 1）全局变量与static变量？（作用域、生存周期）
    * 2）两个.h文件中声明两个同名变量？（使用了与未使用extern） 
    * 3）全局数组和局部数组的初始化？
    * 4）指针和引用的区别？（内存占用、初始化、指向是否可改、作为参数、作为返回）
    * 5）C++的四种强制转换
    * 6）静态类型获取与动态类型获取(typeid、dynamic_cast)
* 二.函数
    * 1）重载（普通函数重载、成员函数重载、继承中的重载、重载与关键字） 
* 三.类
    * 1）面向对象的三大特性（封装、继承、多态）
    * 2）struct和class的区别？
    * 3）访问权限说明符？（目的是加强类的封装性）
    * 4）类的静态成员（所属、声明与定义）
    * 5）构造函数相关
        - 有哪些构造函数（默认、委托、拷贝、移动）
        - 合成的默认拷贝拷贝构造函数（什么情况下不会合成？怎么解决？）
        - 拷贝构造函数（调用时机、合成版的行为、explict？、为何第一个参数必须是引用类型）
        - 移动拷贝构造函数（非拷贝而是窃取资源、与noexcept?、何时合成）
        - 可否通过对象或对象的引用(指针或引用)调用
    * 6）成员初始化列表（顺序，效率）
    * 7）赋值运算符相关
        - 拷贝赋值运算符（合成版的行为？、与delete？、自定义时要注意自赋值、大部分组合了拷贝构造函数与析构函数的工作）
        - 移动赋值运算符（与noexcept？何时合成）
    * 8）析构函数相关
        - 销毁过程的理解（delete的步骤？）
        - 为什么析构函数中不应该抛出异常？
        - 可否通过对象或对象的引用(指针或引用)调用
    * 9）继承相关
        - 继承体系中的构造、拷贝、析构顺序？（派生类只负责自己成员的拷贝控制，在初始值列表或函数体中调用基类的拷贝控制函数完成基类部分的拷贝控制、析构函数不需要显示调用）
        - 继承中的名字查找（作用域嵌套、从子类到父类查找）
        - 同名名字隐藏（如何解决？(域作用符，从指示的类开始查找)、不同作用域无法重载、using的作用？除此之外呢？） 
        - 虚继承（解决什么问题？(多继承中的子对象冗余)）
    * 10）多态的实现？
    * 11）[虚函数的实现原理？对类大小的影响？](https://www.cnblogs.com/malecrab/p/5572730.html)
    * 12）构造、析构函数中调用虚函数？（调用自己的版本）
    * 14）纯虚函数与抽象基类（关系、”=0“、必须在类内申明）
    * 15）静态类型与动态类型（引用是否可实现动态绑定）
    * 16）浅拷贝与深拷贝（安全性、行为像值的类与行为像指针的类）
* 四.容器
    * 1）vector底层的实现？insert具体做了哪些事？resize()调用的是什么？
    * 2）map、set的实现原理（红黑树）
    * 3）map与unordered_map的区别？
* 五.内存管理
    * 1）内存管理有几种方式？（new、delete、malloc、free、allocators）
    * 2）new和malloc的区别？（函数，运算符、类型安全、计算空间、步骤）
    * 3）malloc的实现？
    * 4）delete（步骤、delete与析构、可以delete空指针、可以delete动态const对象）
    * 4）为什么要内存对齐？(性能原因、平台原因)
    * 5）结构体内存对齐方式？（最大成员大小s的整数倍、每个成员偏移分别为0,s,2s..）
    * 6）什么是内存泄露？如何检测与避免？（Mtrace，valgrind）
    * 8）对象复用与零拷贝
    * 9）智能指针相关
        * 种类、区别、原理、能否管理动态数组
        * shared_ptr（使用、计数的变化，get()函数要注意什么）
        * unique_ptr(如何转移控制权)
        * [weak_ptr(特点、用途)](https://www.cnblogs.com/DswCnblog/p/5628314.html)
        * 手写实现智能指针
* 六.关键字
    * 1）extern？（extern "C"?、与static？、有什么问题？）
    * 2）const？（修饰变量、修饰指针与引用、修饰成员函数 《Effective C++:条款3》）
    * 3）mutable？（可变数据成员）
    * 4）static？（修饰变量、类中使用）
    * 5）define与const enum、template inline？（《Effective C++:条款2》、C中默认const是外部连接的，而C++中默认const是内部连接的）
    * 6）explict?（抑制隐式转换、可通过显示转换或直接初始化解决、类外定义时不应重复出现）
    * 7）noexcept？（承诺不会抛出异常）
    * 8）default、delete?（显示要求编译器合成、不能被调用）
    * 9）using？（用于命名空间？、用于类中？）
    * 10）final？（修饰类？、修饰成员函数？）
    * 11）auto？(类型推导、初始化、不能用于函数及模板)
    * 12）volatile?（当对象的值可能在程序的控制或检测之外被改变时(比方说由系统时钟)，应将变量申明为volatile，告诉编译器不应对这样的对象进行优化）
* 七.其它
    * 1）调试程序的方法
    * 2）遇到coredump要怎么调试？
    * 3）内存检测工具的了解
    * 4）模板的用法与适用场景
    * 5）用过C++11？新特性？（auto,decltype、explicit、lambda、final）
    * 6）C++函数调用的压栈过程
    * 7）sizeof和strlen的区别？（运算符与函数、计算的对象、编译时运行时）
    * 8）union？
    * 9）覆盖、重载与隐藏（覆盖要求参数完全相同，用于继承体系的虚函数中，重载要求参数不同）
    * 10）C++是不是类型安全的？（不是，两个不同类型指针可以强制转换）
    * 11）gcc和g++的区别？（gcc代表GUN Compiler Collection，是一堆编译器的集合，包括g++）