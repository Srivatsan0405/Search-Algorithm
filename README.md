# Linear Search and Binary search
## Aim:
To write a program to perform linear search and binary search using python programming.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
## Linear Search:
1.	Start from the leftmost element of array[] and compare k with each element of array[] one by one.
2.	If k matches with an element in array[] , return the index.
3.	If k doesn’t match with any of elements in array[], return -1 or element not found.
## Binary Search:
1.	Set two pointers low and high at the lowest and the highest positions respectively.
2.	Find the middle element mid of the array ie. arr[(low + high)/2]
3.	If x == mid, then return mid.Else, compare the element to be searched with m.
4.	If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.
5.	Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
6.	Repeat steps 2 to 5 until low meets high
## Program:
i)	#Use a linear search method to match the item in a list.
```
''' 
Program for linear search method to match the item in a list
Developed by:SRIVATSAN V
RegisterNumber:23000070
'''
def linearSearch(array,n,k):
    array.sort()
    a=0
    print(array)
    for i in range(n):
        if k==array[i]:
            print("Element found at index: ",i)
            a=1
    if a==0:
        print('Element not found')
array = eval(input())
k = eval(input()) 
n=len(array)
result =linearSearch(array,n,k)


```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
''' 
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by:SRIVATSAN V
RegisterNumber: 23000970
'''
def binarySearchIter(array, k, low, high):
    while low<=high:
        mid = low +(high-low)//2
        if array[mid] ==k:
            return mid
        elif array[mid]<k:
            low=mid+1
        else:
            high=mid-1
    return -1
array = eval(input())
array.sort()
k = eval(input())
result=binarySearchIter(array, k, 0, len(array)-1)
if result==-1:
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)




```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
''' 
Program to find the element in a list using Binary Search (recursive Method).
Developed by: SRIVATSAN V
RegisterNumber: 23000970
'''
def BinarySearch(array, k, low, high):
    if high>=low:
        mid=low+(high-low)//2
        if array[mid]==k:
            return mid
        elif array[mid]>k:
            return BinarySearch(array, k, low, mid-1)
        else:
            return BinarySearch(array, k, mid+1,high)
    else:
        return -1
    
    
    
array = eval(input())
array.sort()
k = eval(input())
result=BinarySearch(array, k, 0, len(array)-1)
if result== -1:
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)




```
## Sample Input and Output
![Screenshot 2023-12-26 102913](https://github.com/Srivatsan0405/Search-Algorithm/assets/139841630/a0237db8-258d-4366-a289-f17a97194777)
![Screenshot 2023-12-26 102925](https://github.com/Srivatsan0405/Search-Algorithm/assets/139841630/a4de1158-5db3-4d8d-9d22-fedfa52f6443)
![Screenshot 2023-12-26 102933](https://github.com/Srivatsan0405/Search-Algorithm/assets/139841630/1e31d9af-b08b-4097-b359-9204027576bf)




## Result
Thus the linear search and binary search algorithm is implemented using python programming.
