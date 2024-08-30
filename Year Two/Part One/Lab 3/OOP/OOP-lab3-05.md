```py
name = input("Enter your name: ")
s = ""
for i in name:
    s += i
    print(s)
 
n=input()
print(n)
try :
    i = int(input("Enter a number: "))
    print(i/0)
    print(i)
except TypeError as e:
    print(f"Error: {e}")
except ValueError as e:
    print("invalid value:", e)
except ZeroDivisionError as e:
    print("error",e)
except:
    print("Last error!")
  
  

i = input("Enter a number: ")
print(i+5)
print(i)

try:
    i = int(input("Enter number: "))
    print(5/2)
except (TypeError, ValueError):
    print("invalid input!")
except:
    print("Last Error")
else:
    print("No Error")
finally:
    print("finally")

  
print( min(20,30) )
print( max(20,30) )
print( max("Ali", "ali") == max('Ali',min('ali','Ali') ))
print( len(" Ahmad ".strip() ))
print( pow(4,2) )
  
import random as r
help(r.randint)
print( r.randint(1,10))

from math import factorial as f, sqrt as s, pi
print( f(5) )
print( s(25) )
print( pi )

import math
print( math.pow(5,2) )
print( pow(5,2) )
print( math.ceil(3.9) )
print( ceil(3.9) )

def name_function() :
    print("User Function")
def int(n):
    return float(n)
x = 5
print( x )
print( int(x) )
print( type(int(x)) )

def print(s):
    print(5)
print("Mohaned")

print( int(5) )
def int(s):
    return f"the value is {s}"
print( int(5) )

def g( x ) :
    if x:
        print("Male")
    else:
        print("Female")

user_input = input("Enter gender ( 0 <= x <= 1 ): ")
try:
    g(bool(int(user_input)))
except:
    print("Error input!")

def function() -> int :
    ...

def get_info():
    print( "Hello" )
def get_info(name):
    print( f"Hello {name}" )
get_info()
```