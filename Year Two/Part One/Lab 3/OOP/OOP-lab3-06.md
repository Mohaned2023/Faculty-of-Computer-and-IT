```py
def g() :
    print("Hello Python")
g()

def g(id, name="Python") :
    print(f"Hi {name}")
g()

def calc( x, y ) :
    return x, y
    
a , b = calc(1,2)
print(type(calc( 1,2 )))
print( a )
print( b )
x  = list(calc(10,20))
print(x)

def return_values():
    return ((10, 20.5, (1,5), True, pow(2,3), [10,20,30] ), )
    
print(len(tuple(return_values())))
print(return_values())
print( return_values()[0][5][1] )

x = (20,)
print(type(x))

def info(*a):
    count = 1
    for i in a[2]:
        print("subject ", count , i )
        count += 1

info()
info( 1 )
info( 1, 2 )
info( 100, "Mohaned", [100,60,70])

def show(**b):
    for i in b:
        print(b[i])
        
show()
show( id=100, name="Mohaned" )

d = dict( id=100, name="Moahned" )
print(d)
show(n=list(d.values()))

def n( *a, **b):
    print(a)
    print(b)
n( 1,2,3, id=100, name="Mohaned")
```