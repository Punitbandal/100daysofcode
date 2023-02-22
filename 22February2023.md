# 1.Arrays-Maximum and Minimum Element in an Array
## The task is to find the maximum and the minimum element of the array using the minimum number of comparisons.
**Input:** arr[] = {3, 5, 4, 1, 9}<br>
**Output:** Minimum element is: 1<br>
            Maximum element is: 9<br>
**Pusdo Code:**
``` python
0)struct  minmax;

1) if(size[arr]==1)
         minmax.min=arr[0]
         minmax.max=arr[0]
         return minmax
2)if(arr[0]>arr[1])
         minmax.min=arr[1]
         minmax.max=arr[0]
  else
        minmax.min=arr[1]
       minmax.max=arr[0]
3)for(int i=2;i<n;i++){
     if (arr[i] > minmax.max)     
            minmax.max = arr[i];
          
     else if (arr[i] < minmax.min)     
            minmax.min = arr[i];
            }
     return minmax
            
```
**C++ Code:**
```c++
 struct Pair{
    int min;
    int max;
};
class Solution
{
   public:
    int findSum(int A[], int N)
    {
    	struct Pair minmax;
    	int num;
    	if (N==1)
    	{
    	    minmax.min=A[0];
            minmax.max=A[0];
    	    return minmax;
    	}
        if(A[0]>A[1])
        {
            minmax.min=A[1];
            minmax.max=A[0];
        }
        else
        {
            minmax.min=A[0];
            minmax.max=A[1];
        }
        
        for(int i=2;i<N;i++){
             if (A[i] > minmax.max)    
            minmax.max = A[i];
             
        else if (A[i] < minmax.min)    
            minmax.min = A[i];
        }
        
        return minmax;
    }

};
```



## 2.Arrays-Reverse the Array	
```
1) Initialize start and end indexes as start = 0, end = n-1

2) In a loop, swap arr[start] with arr[end] and
change start and end as follows :
start = start +1, end = end – 1
```
```c++
void rvereseArray(int arr[], int start, int end)
{
    while (start < end)
    {
        int temp = arr[start];
        arr[start] = arr[end];
        arr[end] = temp;
        start++;
        end--;
    }
}    
```
## 3.Arrays-Maximum-Subarray
