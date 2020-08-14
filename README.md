# -C-函数
第一章 函数的定义和使用
1.1 初见函数
例题：求和，求出1到10、20到30和35到45的三个和。
  思路：笨的方法是copy，也就是代码复制，但这是程序质量不良的表现，以后不易维护。可以把里面重复的代码提出来，可以设立一个函数。
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
