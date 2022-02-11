/*Given an array A of N integers and two integers X and Y, find the number of integers in the array that are both less than or equal to X and divisible by Y.
Input
The first line of the input contains an integer T denoting the number of test cases. The description of each test case follows.
The first line of each test case contains three space separated integers: N, X and Y.
The second line contains N space-separated integers A1, A2, ..., AN denoting the array A.*/

#include<stdio.h>
void main()
{
    int t;
    scanf("%d",&t);
    while(t--)
    {
        int a[1000000],i,n,x,y;
        scanf("%d %d %d",&n,&x,&y);
        for(i=0;i<n;i++)
        {
            scanf("%d",&a[i]);    
        }
        int c=0;
        for(i=0;i<n;i++)
        {
            if(a[i]<=x)
            {
                if(a[i]%y==0)
                {
                    c++;
                }
            }
        }
        printf("%d\n",c);
    }
}
