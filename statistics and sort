#include <stdio.h>
#include <stdlib.h>
//统计文章每个字母出现次数
//按大小排序输出
int swap(int* ,int*);
int swapch(char* ,char* );
int main(int argc,char *argv[])//argc:命令行参数个数，argv[]:每个命令行参数赋入数组
{
    int i,j,figure;
    int ch=0;
    char arr[26];//储存abcd....z字符
    FILE *fp;//文件指针
    int num[26];//统计每个字母出现次数的数组
    for(i=0;i<26;i++)
    {
        arr[i]=97+i;//将abcd...z赋入arr[]中
    }

    for(i=0;i<26;i++)
    {
        num[i]=0;//对数组num[]进行初始化
    }

    if(argc!=2)//判断命令行参量是否未2
    {
        printf("USAGE:%s filename\n",argv[0]);
        return 0;
    }

    if((fp=fopen(argv[1],"r"))==NULL)//排除指定文件为空，fopen(文件，“打开类型”)
    {
        printf("Cant open %s\n",argv[1]);
        return 0;
    }


    while((ch=getc(fp))!=EOF)//在检测到文件结尾前进行循环，统计字母出现次数
    {
        if(ch>64&&ch<97)//大写字母转化为小写字母
        {
            ch=ch+32;

        }
            figure=ch-97;
            num[figure] += 1;

    }

    for(i=0;i<26;i++)//进行冒泡排序，由大到小
    {
        for(j=0;j<i;j++)
        {
            if(num[i]>num[j])
            {
                swap(&num[i],&num[j]);
                swapch(&arr[i],&arr[j]);//两个交换函数使字符数组arr[]与整型num[]形成映射
            }

        }
    }

    for(i=0;i<26;i++)
    {
        printf("%c:%d\n",arr[i],num[i]);//输出排序后的结果
    }
return 0;
}

int swap(int*a ,int*b)
{
    int temp;
    temp=*a;
    *a=*b;
    *b=temp;
    return 0;
}

int swapch(char*a ,char*b)
{
    char temp;
    temp=*a;
    *a=*b;
    *b=temp;
    return 0;
}
