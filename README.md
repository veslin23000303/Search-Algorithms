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
NAME:VESLIN ANISH A
REGISTER NO:212223240175
'''
def search(array,key,n):
    for i in range(0,n):
        if key==array[i]:
            return i
    return -1
array=eval(input())
key=int(input())
array.sort()
n=len(array)
print(array)
result=search(array,key,n)
if result==-1:
    print("Element not found")
else:
    print("Element found at index: ",result)



```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
'''
NAME: VESLIN ANISH A
REGISTER NO:212223240175
'''
def binary(array,key,low,high):
    while(low<=high):
        mid=low+(high-low)//2
        if array[mid]==key:
            return mid
        elif array[mid]<key:
            low=mid+1
        elif array[mid]>key:
            high=mid-1
    return -1
array=eval(input())
key=int(input())
array.sort()
low,high=0,len(array)-1
print(array)
result=binary(array,key,low,high)
if result==-1:
    print("Element not found")
else:
    print("Element found at index: ",result)




```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
#commond line for binary search
#name:VESLIN ANISH A
#reg no:212223240175

def binary(array,key,low,high):
    if(low<=high):
        mid=low+(high-low)//2
        if array[mid]==key:
            return mid
        elif array [mid]<key:
            return binary(array,key,mid+1,high)
        elif array[mid]>key:
            return binary(array,key,low,mid-1)
    return -1
array=eval(input())
key=int(input())
array.sort()
low,high=0,len(array)-1
print(array)
result=binary(array,key,low,high)
if result==-1:
    print("Element not found")
else:
    print("Element found at index: ",result)




```
## Sample Input and Output
![WhatsApp Image 2024-04-22 at 16 39 22_7fa3b829](https://github.com/veslin23000303/Search-Algorithms/assets/151148539/fbff150a-7ba0-452e-8c6f-e36c92d2e67d)
![WhatsApp Image 2024-04-22 at 16 39 07_805529a9](https://github.com/veslin23000303/Search-Algorithms/assets/151148539/194d7a9e-2007-4b22-87ee-9b2198ccfe09)
![WhatsApp Image 2024-04-22 at 16 38 54_3bb9a921](https://github.com/veslin23000303/Search-Algorithms/assets/151148539/78cf2d47-08f5-46cb-83e4-46ee39f06035)






## Result
Thus the linear search and binary search algorithm is implemented using python programming.
