# Basics-python-Programs
# REVERSE A NUMBER
rev = ''
>>> for i in range(len(num), 0, -1):
...     rev += num[i-1]
>>> print(int(rev))
#### Using while loop
def f(n):
    rv=0
    t=n
    while(t!=0):
        r=t%10
        rv=rv*10+r
        t=t//10
    print(rv)
n=int(input())
f(n)


#### AMSTRONG OR NOT
#take input from the user
num = int(input("Enter a number: "))
#initialize sum
sum = 0
#find the sum of the cube of each digit
temp = num
while temp > 0:
   digit = temp % 10
   sum += digit ** 3
   temp //= 10
#display the result
if num == sum:
   print(num,"is an Armstrong number")
else:
   print(num,"is not an Armstrong number")
   
  
  ##### CHECK A NUMBER PRIME OR NOT
from math import sqrt
number = int(input("Enter any number: "))
#prime number is always greater than 1
if number > 1:
    for i in range(2, int(sqrt(number))+1):
        if (number % i) == 0:
            print(number, "is not a prime number")
            break
    else:
        print(number, "is a prime number")
#if the entered number is less than or equal to 1
#then it is not prime number
else:
    print(number, "is not a prime number")
   
   
   #### FIBNOCCI without recursion
def f(n):
    a,b=0,1
    l=[0,1]
    for i in range(1,n-1):
        a,b=b,a+b
        l.append(b)
    print(*l)
n=int(input())
f(n)
#### using recursion
def fibonacci(n):
    if(n <= 1):
        return n
    else:
        return(fibonacci(n-1) + fibonacci(n-2))
n = int(input())
for i in range(n):
    print(fibonacci(i))
    

#### # Recursive Python3 program to check
# if the number is palindrome or not
def rev(n, temp):
	# base case
	if (n == 0):
		return temp;
	# stores the reverse of a number
	temp = (temp * 10) + (n % 10);
	return rev(n // 10, temp);
n = int(input())
temp = rev(n, 0);
if (temp == n):
	print("yes")
else:
	print("no")

