##### **Ques**:



There is a robot located in the cell (a,b) of an infinite grid. Misha wants to move it to the cell (0,0). To do this, he has fixed some integer k. Misha can perform the following operation: 

Choose two integers dx and dy (both from 0 to k inclusive) and move the robot dx cells to the left (in the direction of decreasing x coordinate) and dy cells down (in the direction of decreasing y coordinate). In other words, move the robot from (x,y) to (x−dx,y−dy).



The cost of the operation is:



1, if the chosen pair (dx,dy) is used for the first time;

0, if the pair (dx,dy) has been chosen before.



Note that if dx≠dy, the pairs (dx,dy) and (dy,dx) are considered different.



Help Misha bring the robot to the cell (0,0) with minimum total cost. Note that you don't have to minimize the number of operations.



###### Input:

The first line contains a single integer t (1 ≤ t ≤ 10^4) — the number of test cases.



The only line of each test case contains three integers a, b, and k (1 ≤ a,b,k ≤ 10^18).



###### Output:

For each test case, output a single integer — the minimum total cost of operations required to move the robot to the cell (0,0).





##### **Solution**:



def gcd(a, b):

&nbsp;   while b:

&nbsp;       a, b = b, a%b

&nbsp;   return a

&nbsp;

for \_ in range(int(input())):

&nbsp;   a, b, k = map(int, input().split())

&nbsp;   

&nbsp;   if a>=b:

&nbsp;       g = gcd(a, b)

&nbsp;   else:

&nbsp;       g = gcd(b, a)

&nbsp;

&nbsp;   if max(a//g, b//g)<=k:

&nbsp;       print(1)

&nbsp;   else:

&nbsp;       print(2)

