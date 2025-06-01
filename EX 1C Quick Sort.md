# EX 1C Quick Sort
## DATE:
## AIM:
To write a python program to implement quick sort using tha last element as pivot on the list of float values.

## Algorithm
1. Start by reading n float values from the user and storing them in a list.
2. Define a partition function (qsort) to rearrange elements such that all elements less than or equal to the pivot (last element) are on the left, and the rest on the right.
3. Swap the pivot element into its correct position and return the pivot index.
4. Use the quickSort function to recursively apply the partitioning on sublists to the left and right of the pivot. 
5. After recursion ends, print the sorted array  

## Program:
```python
/*
Program to implement implement quick sort using the last element as pivot on the list of float values.
Developed by: PRADEEP S
Register Number: 212222100034
*/

def qsort(arr,l,h):
    pivot = arr[h]
    i = l-1
    for j in range(l,h):
        if arr[j]<=pivot:
            i+=1
            arr[i],arr[j]=arr[j],arr[i]
    arr[i+1],arr[h] = arr[h],arr[i+1]
    return i+1

def quickSort(arr,l,h):
    if l<h:
        pi = qsort(arr,l,h)
        quickSort(arr,l,pi-1)
        quickSort(arr,pi+1,h)

arr = []
n = int(input())
for i in range(n):
    arr.append(float(input()))
print("Sorted array is:") 
quickSort(arr,0,n-1)
for i in arr:    
    print(i)    
  
```

## Output:

![image](https://github.com/user-attachments/assets/0bb3e20f-4c3c-41a3-acce-9d64527538ec)



## Result:
The program successfully sorts the input array using the QuickSort algorithm, arranging the elements in ascending order.
