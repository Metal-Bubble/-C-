# -C-数组
第一章数组
1.1初试数组
如何写一个程序计算用户输入的数字的平均数？（不需要记录输入的每一个数）
    int x;
    double sum = 0;
    int cnt = 0;
    scanf("%d",&x);
    while( x != -1 ){
      sum += x;
      cnt ++;
      scanf("%d",&x);
     }
     if( cnt > 0 ){
      printf("%f\n",sum/cnt);
     }
如何写一个程序计算用户输入的数字的平均数，并输出所有大于平均数的数？（需要记录每一个数）
如何记录很多数？用数组
         #include <stdio.h>
         int main()
         {
         int x;
         double sum = 0;
         int cnt = 0;
         int number [100];              //定义数组
         scanf("%d",&x);
         while( x != -1 ){
                number[cnt] = x;        //对数组中的元素赋值
                sum += x;
                cnt ++;
                scanf("%d",&x);
         }
         if( cnt > 0 ){
              printf("%f\n",sum/cnt);
              int i;    
              for( i=0; i<cnt; i++){                        //遍历数组
                       if( number[i] > sum/cnt ){           //使用数组中的元素
                                printf("%d\n",number[i]);
                       }
              }
         }
         return 0;
         }
但是这个程序存在安全隐患：我们定义的数组有100个下标，可能不够。

1.2数组的使用：如何定义和使用数组，数组的下标和下标的范围
     
