#include <stdio.h>
#include <stdlib.h>
#include <math.h>
#define N 5000000
//迈克劳林公式：ln(x+1)=x-x ²/ 2+x ³/ 3-....+（-1）＾（n-1）x ⁿ/ n

float Mak(int a);    //利用函数计算公式中的项
int main(void)
{
    float sum;
    int i;

    for(i=1,sum=0;i<N+1;i++)  //将每一项相加
    {
        sum+=Mak(i);
    }

    printf("ln2=%.8f",sum);
    return 0;
}

float Mak(int a)    //计算公式每项：（-1）＾（n-1）x ⁿ/ n
{
    float value,num;
    num=1.00000000/a;
    value=pow(-1,a-1)*pow(1,a)*num;
    return value;

}
