# Remove-Smallest
You are given an array a1,a2,…,an, which is sorted in non-decreasing order (ai≤ai+1).

Find three indices i, j, k such that 1≤i<j<k≤n and it is impossible to construct a non-degenerate triangle (a triangle with nonzero area) having sides equal to ai, aj and ak (for example it is possible to construct a non-degenerate triangle with sides 3, 4 and 5 but impossible with sides 3, 4 and 7). If it is impossible to find such triple, report it.

Input
The first line contains one integer t (1≤t≤1000) — the number of test cases.

The first line of each test case contains one integer n (3≤n≤5⋅104) — the length of the array a.

The second line of each test case contains n integers a1,a2,…,an (1≤ai≤109; ai−1≤ai) — the array a.

It is guaranteed that the sum of n over all test cases does not exceed 105.

Output
For each test case print the answer to it in one line.

If there is a triple of indices i, j, k (i<j<k) such that it is impossible to construct a non-degenerate triangle having sides equal to ai, aj and ak, print that three indices in ascending order. If there are multiple answers, print any of them.

Otherwise, print -1.
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
