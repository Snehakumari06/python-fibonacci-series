# python-fibonacci-series
this is a project provided by my university in which we had to make a python code for fibonacci series.
'''User can enter single or multiple numbers and our system will predict that the entered number or
number's is/are valid number or number's is/are valid number in a fibonacci series or not.'''

#fibonacci no. is a perfect square
import math #using math function(square the number)
def PerfectSquare(x): #using recursion
    s=int(math.sqrt(x)) #Taking s as perfect square
    return s*s==x
#Taking an input in integer  
n=int(input("enter a number:"))
#and also some formulas 
result1=5*(n*n)+4
result2=5*(n*n)-4

sum = 0
n1,n2=0,1
#Putting the condition
if n<=0:
    print("Not valid")
else:
    for i in range(0,n): #Take the loop
        print(sum,end=" ")
        n1 = n2
        n2 = sum
        sum = n1+n2
#call the function        
if PerfectSquare(result1) or PerfectSquare(result2):
    print("\n",n,"is fibonacci number")
else:
    print("\n",n,"is invalid no.")
