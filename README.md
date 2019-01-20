/*1D ARRAY TRAVERSAL*/
#include<stdio.h>
int main()
{
	int arr[50],i,n;
	printf("Enter the no of elements: ");
	scanf("%d",&n);
	printf("Enter %d elements: ",n);
	for(i=0;i<n;i++)
	{
		scanf("%d",&arr[i]);
	}
	printf("Your Array is: ");
	for(i=0;i<n;i++)
	{
		printf("%d ",arr[i]);
	}
	return 0;
}

/*1D ARRAY INSERT ELEMENT*/
#include<stdio.h>
int main()
{
	int arr[50],i,n,value,pos;
	printf("Enter the no of elements: ");
	scanf("%d",&n);
	printf("Enter %d elements: ",n);
	for(i=0;i<n;i++)
	{
		scanf("%d",&arr[i]);
	}
	printf("Enter the insert value: ");
	scanf("%d",&value);
	printf("Enter the insert position: ");
	scanf("%d",&pos);
	if(pos<1 || pos>n+1)
	{
		printf("Insert is not possible!!!");
	}
	else
	{
		for(i=n-1;i>=pos-1;i--)
		{
			arr[i+1]=arr[i];
		}
		arr[pos-1]=value;
		printf("Before insert Array is: ");
		for(i=0;i<n;i++)
		{
			printf("%d ",arr[i]);
		}
		printf("\n");
		printf("After insert Array is: ");
		for(i=0;i<=n;i++)
		{
			printf("%d ",arr[i]);
		}
	}
	return 0;
}

/*1D ARRAY ELEMENT DELETE*/
#include<stdio.h>
int main()
{
	int arr[50],i,n,pos;
	printf("Enter the no of elements: ");
	scanf("%d",&n);
	printf("Enter %d elements: ",n);
	for(i=0;i<n;i++)
	{
		scanf("%d",&arr[i]);
	}
	printf("Enter the position to delete element: ");
	scanf("%d",&pos);
	if(pos<1 || pos>n)
	{
		printf("Deletion is not possible!!!");
	}
	else
	{
		printf("Before delete Array is: ");
		for(i=0;i<n;i++)
		{
			printf("%d ",arr[i]);
		}
		printf("\n");
		for(i=pos-1;i<n;i++)
		{
			arr[i]=arr[i+1];
		}
		printf("After delete Array is: ");
		for(i=0;i<n-1;i++)
		{
			printf("%d ",arr[i]);
		}
	}
	return 0;
}

/*1D ARRAY ASCENDING & DESCENDING ORDER*/
#include<stdio.h>
int main()
{
	int arr[50],i,j,n,swap;
	printf("Enter the no of elements: ");
	scanf("%d",&n);
	printf("Enter %d elements: ",n);
	for(i=0;i<n;i++)
	{
		scanf("%d",&arr[i]);
	}
	printf("Your original Array: ");
	for(i=0;i<n;i++)
	{
		printf("%d ",arr[i]);
	}
	printf("\n");
	for(i=0;i<n;i++)
	{
		for(j=0;j<n;j++)
		{
			if(arr[j]>arr[i])
			{
				swap=arr[i];
				arr[i]=arr[j];
				arr[j]=swap;
			}
		}
	}
	printf("Array in ascending order: ");
	for(i=0;i<n;i++)
	{
		printf("%d ",arr[i]);
	}
	printf("\n");
	for(i=0;i<n;i++)
	{
		for(j=0;j<n;j++)
		{
			if(arr[j]<arr[i])
			{
				swap=arr[i];
				arr[i]=arr[j];
				arr[j]=swap;
			}
		}
	}
	printf("Array in descending order: ");
	for(i=0;i<n;i++)
	{
		printf("%d ",arr[i]);
	}
	return 0;
}

/*ARRAY LARGEST & SMALLEST ELEMENT*/
#include<stdio.h>
int main()
{
	int arr[50],i,n,large,small;
	printf("Enter the no of elements: ");
	scanf("%d",&n);
	printf("Enter %d elements: ",n);
	for(i=0;i<n;i++)
	{
		scanf("%d",&arr[i]);
	}
	printf("Your Array is: ");
	for(i=0;i<n;i++)
	{
		printf("%d ",arr[i]);
	}
	printf("\n");
	large=small=arr[0];
	for(i=0;i<n;i++)
	{
		if(arr[i]>large)
		{
			large=arr[i];
		}
	}
	for(i=0;i<n;i++)
	{
		if(arr[i]<small)
		{
			small=arr[i];
		}
	}
	printf("Largest elements is: %d\n",large);
	printf("Smallest element is: %d",small);
	return 0;
}
