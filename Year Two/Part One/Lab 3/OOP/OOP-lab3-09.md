```Python
Books=[]

class Book:
    ID = 0
    title = None
    author = None
    publisher = None
    publish_data = None

	def info(self):
        print(f"ID: {self.id}")
        print(f"title: {self.title}")
        print(f"author: {self.author}")
        print(f"publisher: {self.publisher}")
        print(f"publish data: {self.publish_data}")
    def add(self):
        self.ID = input("Enter book id: ")
        self.title = input("Enter book Title: ")
		self.author = input("Enter the author name: ")
        self.publisher = input("Enter book publisher: ")
        self.publish_data = input("Enter publish data: ")
        Books.append(self)

b = Book()
B = b()
print( B )

class A:
    a = None
    def __init__(self):
        print('New copy added..')
    def __init__(self, a=None):
        self.a = a
        print(self.a)

a = A(400)
b = A()

class Person:
    ID = 0
    name = None
    age = 0
    gender = True
    def __init__(self, name):
        self.name = name

    @staticmethod
    def info():
         # return "Perosn"
        return f'ID: {self.ID}, name: {self.name}, age: {self.age}, gender: {self.gender}'

class Student(Person):
    def __init__(self, id, name):
        self.ID = id
        self.name = name
    level = 0

class Emp(Person):
    hierDate = None
    def info(self):
        return "Emp " + Person.info()

s = Student( 100, "Mohaned" )
print(  s.info()  )
e = Emp("Moahe")
print( e.info() )

class A:
    a = None
class B(A):
    b = None
class C(B):
    c = None
obj = C()

print( obj.a )
print( obj.b )
print( obj.c )

class D:
    d = None
    def Info(self):
        print("D")
class E(C):
    e = None
    def info(self):
        print("E")
class F(D,E):
    pass

obj = F()
obj.info()
print( F.mro() )
```