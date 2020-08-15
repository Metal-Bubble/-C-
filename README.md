# -C-函数
第一章 函数的定义和使用
1.1 初见函数
例题：求和，求出1到10、20到30和35到45的三个和。
  思路：笨的方法是copy，也就是代码复制，但这是程序质量不良的表现，以后不易维护。可以把里面重复的代码提出来，可以设立一个函数
  代码：
   #include <stdio.h>
   void sum ( int begin, int end )
   {
      int i;
      int sum = 0;
      for ( i = begin; i <= end; i++)
      {
        sum += i;
      }
      printf("%d到%d的和是%d\n", begin, end, sum);
   }
   
   int main()
   {
    sum(1,10);
    sum(20,30);
    sum(35,45);
    
    return 0;
   }

1.2 函数定义和调用
什么是函数：函数是一块代码，接收零个或多个参数，做一件事情，并返回零个或一个值
函数定义：函数头+函数体
	函数头=返回类型+函数名+参数表 
调用函数：
	函数名（参数值）
	（）起到了表示函数调用的重要作用
	即使没有参数也需要（）
	如果有参数，则需要给出正确的数量和顺序
	这些值会被按照顺序依次用来初始化函数中的参数
	
1.3 从函数中返回
return：return停止函数的执行，并送回一个值
	两种形式：1、return； 2、return 表达式；
	一个函数里可以出现多个return语句
例一：
int max( int a,int b)
{
	int ret;
	if( a > b){
		ret = a;
	}else{
		ret = b;
	}
	return ret;
}
例二:
int a,b,c;
a = 5;
b = 6;
c = max(10,12);
c = max(a,b);
c = max(c,23);
c = max(max(c,a),5);
printf("%d\n",max(a,b));
max(12,13);
由例子可以看出从函数中返回的值：
	可以赋值给变量
	可以再传递给函数
	甚至可以丢弃，也就是不赋值给别的变量
没有返回值的函数
	void函数名（参数表）
	不能使用带值的return
	可以没有return
	调用的时候不能做返回值的赋值
但如果函数有返回值，则必须使用带值的return


第二章 函数的参数和变量
2.1 函数原型：用来告诉编译器这个函数长什么样
函数先后关系：C的编译器自上而下顺序分析你的代码
例子：
#include <stdio.h>
   void sum ( int begin, int end )											
   {
      int i;
      int sum = 0;
      for ( i = begin; i <= end; i++)
      {
        sum += i;
      }
      printf("%d到%d的和是%d\n", begin, end, sum);
   }
   
   int main()
   {
    sum(1,10);      //在看到sum（1，10）的时候，它需要知道sum（）的样子，也就是sum（）要几个参数，每个参数的类型如何，返回什么类型
    sum(20,30);																							
    sum(35,45);
    
    return 0;
   }
如果
	

			

	
