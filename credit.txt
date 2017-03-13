#include <stdio.h>
#include<cs50.h>
int main()
{
    int sum1=0,sum2=0,c=0,a[100],i=0,sum;
     long long int num;
    printf("Enter any number to find sum of its digit: ");
    scanf("%lli", &num);
    while(num!=0)
    {
        
        a[c]=num%10;
        c++;
        num = num / 10;
    }
    for(i=0;i<c;i++)
    {
        printf("%d\n",a[i]);
    }
    for(i=1;i<c;i+=2)
    {
           
        sum1+=((a[i]*2)/10)+((a[i]*2)%10);
    }
    for(i=0;i<c;i+=2)
    {

        sum2+=(a[i]);
    }
    sum=sum1+sum2;
    if(sum%10==0)
        printf("AMEX");
    else
        printf("INVALID");

    return 0;
}
