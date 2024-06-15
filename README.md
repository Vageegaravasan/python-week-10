1.
def bubble_sort(arr):
    n = len(arr)
    swaps = 0

    for i in range(n):
        for j in range(n - 1):
            if arr[j] > arr[j + 1]:
                arr[j], arr[j + 1] = arr[j + 1], arr[j]
                swaps += 1

    return swaps

def main():
    n = int(input().strip())
    arr = list(map(int, input().strip().split()))

    swaps = bubble_sort(arr)

2.
n=int(input())
s=input().split()
k=[int(x) for x in s]
sum=int(input())
c=1
for i in k:
    for j in k:
        if i+j==sum and c!=0 and len(k)==n:
            print("Yes")
            c=0
           
if c==1:
    print("No")

3.

k=[int(x) for x in input().split()]
list1=[0]*100
k.sort()
for i in k:
    list1[i]+=1
s=[]    
for i in k:
    if i not in s:
        s.append(i)
for i in s:
    print(i,list1[i])

4.
def find_peak_elements(arr):
    n = len(arr)
    peaks = []

    if arr[0] >= arr[1]:
        peaks.append(arr[0])

    for i in range(1, n - 1):
        if arr[i] >= arr[i - 1] and arr[i] >= arr[i + 1]:
            peaks.append(arr[i])

    if arr[n - 1] >= arr[n - 2]:
        peaks.append(arr[n - 1])

    return peaks

def main():
    n = int(input().strip())
    arr = list(map(int, input().strip().split()))

    peak_elements = find_peak_elements(arr)

    print(*peak_elements)

if __name__ == "__main__":
    main()

5.
def bubble_sort(arr):
    n = len(arr)
    for i in range(n):
        for j in range(0, n-i-1):
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]

def main():
    n = int(input())
    arr = list(map(int, input().split()))

    bubble_sort(arr)

    for num in arr:
        print(num, end=" ")

if __name__ == "__main__":
    main()


