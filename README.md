# Mycode_repo
DSA code
#include<stdio.h>
#define SIZE 5

int main()
{
	int i,hole,temp;
	int arr[SIZE];
	for(i = 0; i<SIZE-1; i++)
	{
		printf("The %d element of the array is:",i+1);
		scanf("%d",&arr[i]);
	}
	for(i = 0; i<SIZE-1; i++)
	{
		temp = arr[i];
		hole = i;
		while(hole>0 && arr[hole-1] >temp)
		{
			arr[hole] = arr[hole-1];
			hole--;
		}
		arr[hole] = temp;
	}
	printf("The sorted array is\n");
	for(i= 0; i<SIZE-1; i++)
	{
		printf("%d-->",arr[i]);
	}
	return 0;
}
