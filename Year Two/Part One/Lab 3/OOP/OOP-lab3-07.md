```py
import calendar
print(calendar.calendar(2024))
print(calendar.month(2024,8))  

name = "Ahmed"
print(name[1])
print(name[-4])
print(name[:2])
print(name[2:])
print(name[2:] + name[:2] )
print(name[:2] + name[2:] )
print( name[::2] )
print( name[::2][::2] )
print( name[::4] )
print( name[::-1] )
print( name[-1::2] )
print( name[-1::-2] )
print( name[3::-2] )
  
date = ['31', '08', '2024']
print( '/'.join(date) )
print( 'Ahmed'.join(date) )

n = "100 Moahned 23 Male"
m = n.split(' ')
print(m)
print(   f"ID:" + m[0]  )
print(   f"name:" + m[1]  )
print(   f"age:" + m[2]  )
print( ','.join('123456789') )
print( ','.join('123456789').split(',') )

name = "Mohaned Sherhan "
print(name.upper())
print(name.lower())
print(name.swapcase())
print(name.title())
print(name.capitalize())
print( name.islower() )
print( name.isupper() )
print( name.istitle() )
print( name.lower().istitle() )
print( str(name.islower()) )
print( str(name.islower()).istitle() )
print(   name.count('m')   )
print(   name.lower().count('m')   )
print(   name.count('m'.upper())   )
print( name.title().swapcase().swapcase().istitle() )
print( -1-1*name[::-1].find(' ') )
print( name.replace('e','$') )
print( name.startswith('MO') )
print( name.endswith('e') )
print ( name[-1::2].isspace() )
print ( name[-1::-2].isspace() )
print( ''.replace('','  ').isspace() )
print( name.replace('', '#') )
print( '123'.isdigit() )
print( '1'.isdigit() )
print( 'A2'.isdigit() )
print( len(name) )
print(    name.center( len(name) )    )
print(    name.center(40)    )
print(    name.center(40, '+')    )
print(    name.center(43, '+')    )

id = 100
name = "Mohaned"
age = 22
print(  "id %d name %s age %d"%(id, name, age)  )
print(  "id %d name %s age %d"%(id, name)  ) # error
print(  "id %d name %s age %d selery %.2f"%(id, name, age, 300.3)  )
print(  "id %d name %s age %d selery %.2f"%(id, name, age, 300.375)  )

L0 = []

print(L0)
print(type(L0))

L0[0] = 100 # error

L0.append(1000)
L0[0] = 100
print(L0)

L1 = L0
L1[0] = 200
L1 += L0

print(L0)
print(L1)  

L0 = [1,2]
L1 = [10,20]

L0.append(L1)
L0.extend(L1)
L0.insert(1,2000)
L0.pop(0)
L0.remove(2000)
L0.sort()
L0.sort(reverse=True)
L0.reverse()

print(L0)
```