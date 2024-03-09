# Data_Structure_Binary_Search

#include<stdio.h>
int BinarySearch(int arr[] , int size , int element){
    int low,mid,high;
    low =0 ;
    high = size-1;
    while(low<=high){
        mid = (low+high)/2;
        if(arr[mid]==element){
            return mid;
        }
        else if (arr[mid]<element){
            low = mid+1;
        }
        else {
            low= mid-1;
        }
    }
    return -1;
}

int main(){
    // sorted array
    int arr[] = {1,4,6,9,34,98,101,123};
    int size = sizeof(arr)/sizeof(int);
    int element = 101;
    int SearchIndex = BinarySearch(arr, size ,element);
    printf("The element was found at %d index" , SearchIndex);

    return 0;
}
