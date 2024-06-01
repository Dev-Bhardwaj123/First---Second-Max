# First---Second-Max
Finding first maximum and second maximum element in an array 
//Finding max and second max
#include<iostream>
#include<algorithm>
using namespace std;

int main(){
	int n;
	cout<<"Enter size of array: ";
	cin>>n;
	int arr[n];
	for(int i=0;i<n;i++){
		cin>>arr[i];
	}
	
  //1 st method
	int max=arr[0];
	for(int i=1;i<n;i++){
		if(arr[i]>max){
			max=arr[i];
		}
	}
	cout<<"Max element is: "<<max<<endl;
	int sec_max=arr[0];
	for(int i=1;i<n;i++){
		if(arr[i]>sec_max && arr[i]!=max){
			sec_max=arr[i];
		}
	}
	cout<<"Second max is: "<<sec_max;
	
  //2 nd method
	sort(arr,arr+n);
	cout<<"Max ele is: "<<arr[n-1]<<endl;
	cout<<"Second max ele is: "<<arr[n-2]<<endl;
	return 0;
}
