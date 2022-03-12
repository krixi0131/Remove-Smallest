# Remove-Smallest
```python
t=int(input())
for count in range(t):
    n=int(input())
    a=list(map(int,input().split()))
    a.sort()
    check=0
    for i in range(n-1):
        if a[i+1]-a[i]>1:
            check=1
    if check==1:
        print("NO")
    elif check==0:
        print("YES")
```
