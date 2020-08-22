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
         int number [100];
         scanf("%d",&x);
         while( x != -1 ){
                number[cnt] = x;
                sum += x;
                cnt ++;
                scanf("%d",&x);
         }
         if( cnt > 0 ){
              printf("%f\n",sum/cnt)
         }
         return 0;
         }
