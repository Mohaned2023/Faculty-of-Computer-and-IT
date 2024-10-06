```Python
s = "Python"
print( s[::2][::3] )
print( s[::-2][::3] )
print( s[-3::2] )

s = "Ali"
a = "Ahmed"
print( type(s) )
print( type(a) )

class Greet:
    msg = "Hello Python"
    def print_msg( self ):
        self.Greet()
        print( Greet.msg )
        print( self.msg ) # g0.msg
        print("----------")

    def Greet( self ):
        print("Welcom MR")
    def Greet( self, name=None ):
        if name == None:
            print( "Welcom" )
        else:
            print( f"Welcom {name}" )

g0 = Greet()
g1 = Greet()
g0.msg = "Hi Python"
Greet.msg =  "Welcom Python"
print(g0.msg)
g1.msg = "Welcom Python"
print(g1.msg)
g0.print_msg()
g1.print_msg()
g0.Greet()
g1.Greet("Mohaned")

class Student:
    student_id = None
    gender = True
    name = None
    level = None

    def info(self):
        print( f"ID: {self.student_id}" )
        print( f"Gender: {self.getGender()}" )
        print( f"name: {self.name}" )
        print( f"level: {self.level}" )

	def getGender(self):
	    if self.gender:
            return "Male"
        return "Famel"

man = Student()
man.student_id = 24164018
man.name = "Mohaned"
man.level = "IT2"
man.info()

class Student:
    SID=None
    SName=None
    Gender=True
    Level=None

    def Info(self):
        print(f"ID {self.SID} NAme {self.SName} Gender"
        f"{self.GetGender()} Level {self.Level}")
    def GetGender(self):
        if self.Gender:
            return "Male"
        else:
            return "Female"

s0=Student()
s0.SID=1000
s0.SName="Raeif"
s0.Level=2
s0.Info()

class MyMath:
    x = 0
    y = 0
    def sum(self):
        return self.x + self.y
    def sub(self):
        return self.x - self.y
    def mul(self):
        return self.x * self.y
    def div(self):
        try:
            return self.x / self.y
        except ZeroDivisionError as e:
            return e
        except Exception as e:
            return e

m = MyMath()
m.x = 20
print( m.sum() )
print( m.sub() )
print( m.mul() )
print( m.div() )
```