# EX 1B Merge Sort
## DATE:
## AIM:
To write a python program to sort the first half of the list using merge sort.

## Algorithm
1. Input the number of elements n and the array arr.
2. Define mergeSort(arr): If len(arr) > 1, divide the array into two halves and recursively sort        each half.
3. Merge the two sorted halves by comparing elements and combining them back into arr.
4. Define printList(arr): Print each element of the array.
5. Call mergeSort(arr) to sort the array and print the result.


## Program:
```
/*
Program to implement Merge Sort
Developed by: SWETHA P
Register Number:  212222100053
*/

def mergeSort(arr):
    if len(arr) > 1:
        mid = len(arr) // 2 
        L = arr[:mid]
        R = arr[mid:]
        
        mergeSort(L)
        mergeSort(R) 
        
        i = j = k = 0
        
   
        while i < len(L) and j < len(R):
            if L[i] < R[j]:
                arr[k] = L[i]
                i += 1
            else:
                arr[k] = R[j]
                j += 1
            k += 1
        

        while i < len(L):
            arr[k] = L[i]
            i += 1
            k += 1
        
        while j < len(R):
            arr[k] = R[j]
            j += 1
            k += 1

def printList(arr):
    for i in range(len(arr)):
        print(arr[i], end=" ")
    print()

n = int(input())
arr = []
for i in range(n):
    l = int(input())
    arr.append(l)

print("Given array is")
printList(arr)

mergeSort(arr)

print("Sorted array is")
printList(arr)
```

## Output:
![image](https://github.com/user-attachments/assets/4484adec-5f3d-47e5-bcd5-bb80a785dd82)

## Result:
The program successfully sorts a given list of values using the Merge Sort algorithm, displaying the sorted result.
