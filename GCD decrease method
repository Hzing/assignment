#include <stdio.h>
#include <stdlib.h>
int GCD(int ,int );
void SUB(int *,int *);
int main(void)
{
    int a,b,num;
    scanf("%d %d",&a,&b);
    num=GCD(a,b);
    printf("最大公约数为%d",num);
    return 0;
}
int GCD(int a,int b)
{
    int temp;

    for(temp=1;0==a%2&&0==b%2;temp*=2)
    {
        a/=2;
        b/=2;
    }
    while((0!=a%2||0!=b%2)&&a!=b)
    {
        SUB(&a,&b);
    }
    if(a==b)
    {
        return temp*a;
    }
}

void SUB(int *a,int *b)
{
    int tran;
    if(*a>*b)
    {
        tran=*b;
        *b=*a-*b;
        *a=tran;
    }
    else
    {
        tran=*a;
        *a=*b-*a;
        *b=tran;
    }

}
