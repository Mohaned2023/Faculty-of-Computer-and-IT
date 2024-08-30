
```py
x = 5

y = 2

print( x + y )

print( x - y )

print( x * y )

print( x ** y )

print( x / y )

print( x // y )

print( True and True )

print ( True or False )

print ( not(True) )

print( not(not(not(0 and not(1) )) or 1 ))

print ( type(True + True) )

print( bool(0) )

print( True and 5 )

print( 5 and True  )

print( True or 5 )

print( 5 or True  )

x = 5

y = 6

print( x & y )

print( x | y )

print( x ^ y )

print(bin(x))

print(bin(y))

print( bin(y << x) )

print( x >> 2 )

"""

if ( x > 0 ) {

    cout << "+";

}

else {

    cout << "-";

}

"""

x = 1

if x > 0 :

    print( "+" )

    print( "++" )

else:

    print( "-" )

x = int (input("Enter a Number: "))

if x == 0 :

    print( "Zero" )

else :

    if x%2 == 0:

        print(x**2)

    else:

        print(x**3)

user_input = int(input("Enter the degree: "))

if user_input in range(0,101) :

    if user_input >= 50:

        if user_input >= 90:

            print( "A" )

        elif user_input >= 80:

            print( "V.G" )

        elif user_input >= 65:

            print("G")

        else:

            print("pass")

    else:

        print("Filed")

else:

    print("Error input!")

x = 0

while x < 10 :

    x += 2

    print( x )

f = int(input("Enter a number: "))

m = 1

while f > 1:

    m *= f

    f -= 1

print( m )

i = 0

while i <= 10 :

    print( "*" * i )

    i += 1

i = 0

while i < 10 :

    print(  (10-i) * ' ' + "*" * i + "*" * i )

    i += 1

while i > 0 :

    print(  (10-i) * ' ' + "*" * i + "*" * i )

    i -= 1
```