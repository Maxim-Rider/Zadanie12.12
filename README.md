# Zadanie12.12
#1
n, m = [int(i) for i in input().split()]
a = [[int(j) for j in input().split()] for i in range(n)]
best_i, best_j = 0, 0
curr_max = a[0][0]
for i in range(n):
    for j in range(m):
        if a[i][j] > curr_max:
            curr_max = a[i][j]
            best_i, best_j = i, j
print(best_i, best_j)

#2    
n = int(input())
a = [['.'] * n for i in range(n)]
for i in range(n):
    a[i][i] = '*'
    a[n // 2][i] = '*'
    a[i][n // 2] = '*'
    a[i][n - i - 1] = '*'
for row in a:
    print(' '.join(row))
#3
n = int(input('n = '))
m = int(input('m = '))
r = [['.*'[(j + i) % 2] for j in range(m)] for i in range(n)]
print(r)
#4
n = int(input())
a = [[abs(i - j) for j in range(n)] for i in range(n)]
for row in a:
    print(' '.join([str(i) for i in row]))
#5
n = int(input())
a = [[0] * n for i in range(n)]
for i in range(n):
    a[i][n - i - 1] = 1
for i in range(n):
    for j in range(n - i, n):
        a[i][j] = 2
for row in a:
    for elem in row:
        print(elem, end=' ')
    print()
#6
from random import random
M = 10
N = 5
a = []
for i in range(N):
    b = []
    for j in range(M):
        b.append(round(random()*2))
    a.append(b)
    print(b)
 
c1 = int(input("Один столбец: ")) - 1
c2 = int(input("Другой столбец: ")) - 1

for i in range(N):
    a[i][c1], a[i][c2] = a[i][c2], a[i][c1]
    print(a[i])
#7
n=int(input())
m=int(input())
[i][j]=i*j
for j in range(m):
    a.append([int(j)for j in input().split()])
for i in range(n):
    a.append([int(i)for i in input().split()])





