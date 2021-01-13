/******************************************************************************

                              Online C++ Compiler.
               Code, Compile, Run and Debug C++ program online.
Write your code in this editor and press "Run" button to compile and execute it.

*******************************************************************************/

#include <iostream>
using namespace std;


int main()
{
	//array declaration
	int arr[100];
	int n,i,j;
	int temp;
	
	//Total number to be read
	cout<<"Enter number of elements to be read: ";
	cin>>n;
	
	//check bound
	if(n<0 || n>100)
	{
		cout<<"Input valid range!!!"<<endl;
		return -1;
	}
	
	
	for(i=0;i<n;i++)
	{
		cout<<"Enter Number ["<<i+1<<"] ";
		cin>>arr[i];
	}
	
	//print input number
	cout<<"Unsorted Array:"<<endl;
	for(i=0;i<n;i++)
		cout<<arr[i]<<"\t";
	cout<<endl;
	
	//sorting - ASCENDING ORDER
	for(i=0;i<n;i++)
	{		
		for(j=i+1;j<n;j++)
		{
			if(arr[i]>arr[j])
			{
				temp  =arr[i];
				arr[i]=arr[j];
				arr[j]=temp;
			}
		}
	}
	
	//print sorted array 
	cout<<"Sorted Array (Ascending Order):"<<endl;
	for(i=0;i<n;i++)
		cout<<arr[i]<<"\t";
	cout<<endl;	
	
	//sorting - Descending ORDER
	for(i=0;i<n;i++)
	{		
		for(j=i+1;j<n;j++)
		{
			if(arr[i]<arr[j])
			{
				temp  =arr[i];
				arr[i]=arr[j];
				arr[j]=temp;
			}
		}
	}
	
	//print sorted array 
	cout<<"Sorted Array (Descending Order) :"<<endl;
	for(i=0;i<n;i++)
		cout<<arr[i]<<"\t";
	
	cout<<endl;
	
	return 0;
	
}

