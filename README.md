# RotationOfArray
DSA

package com.abirham;

public class RotateArrayS {
    public static void main(String[] args) {
        int []arr={1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,6,17,18};
        int N=arr.length;
        int d=2;
        rotate(arr,N,d);
        printArray(arr,N);
    }
    public static  void  rotate(int arr[], int n, int d){
        int temp[]=new int[n];
        int k=0;
        for(int i=d;i<n;i++)
        {
            temp[k]=arr[i];
            k++;

        }
        for(int i=0;i<d;i++)
        {
            temp[k]=arr[i];
            k++;
        }
        for(int  i=0;i<n;i++)
        {
            arr[i]=temp[i];
        }
    }
    public static void printArray(int arr[],int n)
    {
        for(int i=0;i<n;i++)
        {
            System.out.print(arr[i]+" ");

        }
    }
}
