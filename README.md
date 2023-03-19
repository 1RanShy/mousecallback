# Materials

This is a branch to stroe all materials about emmbeded system.

1. 我在这里面写了自己对于老师的mousecallback 这个工程文件的解释
2. 可以由此看出我们应该如何构建我们的 embeded system

---

~~~text
1. 在每一个线程中都有一个thread
2. mouse.cpp中可以看到 mouse这个函数得到的返回值都是不会外传的,直接复制给callback函数处理
~~~

---

~~~c++
void Mouse::start()
{
 t = thread(&Mouse::ReadMouse, this);
}
~~~

这种创建线程的方式是: Non-static member function 非静态成员函数创建变量
这是为了在不创建类的对象的情况下使用其中的成员函数, 这是要加上this的.在实例化类了之后要加上&object,没有实例化类的时候时候就是this.
详情参见:
[C++ ,ultithread - YouTube](https://www.youtube.com/results?search_query=C%2B%2B+%2Cultithread)
的第二章

---

创建线程的方式共有:

~~~text
Five different types for creating threads. 
1. Function Pointer -- this is the very basic form of creating threads. 
2. Lambda Function 
3. Functor (Function Object) 
4. Non-static member function
5. Static member function
~~~
