# C-p87-2-1-
C语言学习笔记 p 87 函数
//接上
//判断是否是闰年
#include<stdio.h>
is_leap_year(int y)
{
    if(y%4==0&&y%100!0)||(y%400==0))
        return 1;
    else
        return 0;
}//函数尽量设置单一，让函具有可移植性
int main()
{
    int year=0;
    for(year=1000;year<=2000;year++)
    {
        //判断year是否为闰年
        if(1=is_leap_year())
        {
            printf("%d",year);
        }
    }
  return 0;
}



int binary_search(int arr[],int k,int sz)/本质上arr是一个指针
{
    //算法的实现
    
    int left=0;
    int right=sz-1;
    
    while(left<=right)
    {
        int mid=(left+right)/2;//中间元素的下标
        if(arr[mid]<k)
       {
            left=mid+1;
       }
        else if(arr[mid]>k)
        {
            right=mid-1;
        }
        else
        {
            return mid;
        }
    }
}
int main()
{
    //二分查找
    //在一个有序数组中查找具体某个数
    //如果找到返回下标，找不到返回-1
    int arr[]={1,2,3,4,6,7,8,9,10};
    int k=7;
    int sz=sizeof(arr)/sizeof(arr[0]);
    int k=7;
    int ret=binary_search(arr,k,sz);//这里实际传过去的是首元素的地址
    int k=7;
    if(ret==-1)
    {
        printf("找不到指定的数字\n);
    }
    else
    {
        printf("找到了，下标是：%d\n",ret);
    }
    return 0;
}



void Add(int* p)
{
    (*p)++;//++优先级较高，所以*p需要括起来
}
int main()
{
    int num=0;
    Add(&num);
    printf("num=%d\n",num)//1
    Add(&num);
    printf("num=%d\n",num)//2
    Add(&num);
    printf("num=%d\n",num)//3
    return 0;
}


//函数的嵌套调用和链式访问
//链式访问：把一个函数的返回值返回另一个函数的参数
int mian()
{
    int len=0;
    //1
    len=strlen("abc");
    printf("%d\n",len);
    //2
    printf("%d\n",strlen("abc"));
    return 0;
}


int main()
{
    printf("%d",printf("%d",printf("%d",43)));
    return 0;
}



//函数的声明和定义
//函数声明：放在头文件里，先声明后使用
int Add(int x,int y);

int main()
{
    int a=10;
    int b=20;
    int sum=0;
    //函数调用
    sum=Add(a,b);
    printf("%d\n",sum);
    return 0;
}
//函数定义
int Add(int x,intr y)
{
    int z=x+y;
    return z;
}




