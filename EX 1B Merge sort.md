# EX 1B Merge Sort
## DATE:
## AIM:
To write a python program to sort the first half of the list using merge sort.

## Algorithm
1. Start by reading the number of elements n and take input for the array elements.
2. Divide the array into two halves: first_half and sec_half.
3. Apply the merge sort algorithm only to the desired half (either first or second) based on a condition.
4. In the merge_sort function, recursively divide the list until each sublist contains one element. 
5. Merge the sublists in sorted order and combine the sorted half with the unchanged other half.  

## Program:
```python
/*
Program to implement Merge Sort
Developed by: PRADEEP S
Register Number: 212222100034 
*/

def merge_sort(arr):
    if len(arr)>1:
        mid = len(arr)//2
        
        left = arr[:mid]
        right = arr[mid:]
        
        merge_sort(left)
        merge_sort(right)
        
        i=0
        j=0
        k=0
        
        while i<len(left) and j<len(right):
            if left[i]<right[j]:
                arr[k] = left[i]
                i+=1
                k+=1
            else:
                arr[k] = right[j]
                j+=1
                k+=1
        while i<len(left):
            arr[k] = left[i]
            i+=1
            k+=1
        while j<len(right):
            arr[k] = right[j]
            j+=1
            k+=1
    return arr
    
n = int(input())
mid = n//2
arr = []
for i in range(n):
    arr.append(int(input()))
    
first_half = arr[:mid]
sec_half = arr[mid:]
print("Given array is")
print(*arr)
print()
print("Sorted array is")
if max(first_half) < max(sec_half):
    arr = merge_sort(first_half)+sec_half
    print(*arr)
else:
    arr = merge_sort(sec_half) + first_half
    print(*arr)
            
            
```

## Output:

![image](https://github.com/user-attachments/assets/faabb961-80d9-4d61-a037-6f2bb989e15f)



## Result:
The program successfully sorts the first half of the given array using merge sort. where only the first half is sorted, and the second half remains unchanged.
