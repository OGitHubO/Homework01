#include<iostream>
#include<stdio.h>
#include<stdlib.h>

int main()
{
	int a[100], max, i, n, flag, j, sum;
	scanf("%d", &n);
	for(i=0;i<n;i++)
	{
		scanf("%d", &a[i]);
	}
	max=0;
	flag=0;
	for(i=0;i<n;i++)
	{
		max=max+a[i];
		if(a[i]>=0)
		{
			flag=1;
		}
	}
	for(j=n-1;j>=0;j--)
	{
		sum=0;
		for(i=0;i<=j;i++)
		{
			sum=sum+a[i];
		}
		if(sum>max)
		{
			max=sum;
		}
	}
	if(flag==1)
	{
		printf("最大子段和为：%d", max);
	}
	else
	{
		printf("最大子段和为：0");
	}
	system("pause");
	return 0;
}
