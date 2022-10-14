id:"1"

Topic: "DSA-Searching"

Question: "WAP to search particular target in an given array in O(log n ) time"


def binary(l,s,e,k):
    start=s
    end=e
    mid=start+(end-start)//2
    while(start<=end):
        if(l[mid]==k):
            return mid
        if(k<l[mid]):
            start=mid+1
        else:
            end=mid-1
        mid=start+(end-start)//2
    return -1

l=[2,3,5,8]
//l=list(map(int,input().split()))
k=int(input())
n=len(l)
print(binary(l,0,n-1,k))
