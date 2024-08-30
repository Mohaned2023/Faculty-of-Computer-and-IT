```py
"""
# Enter degree for 6 subjects.
    if the degree is valide => for
    find the avg and the sum of the 6 sub
"""

def main() -> None:
    SUB_NUMBER: int = 6
    i: int = 0
    degrees: list[int] = []
    avg: float = 0.0
    while i<6:
        try:
            degree: int = int(input(f"Enter the degree for the subject {i+1}: "))
            if degree < 0 or degree > 100 :
                print( "The degree most be in range of ( 0 <= x <= 100 )!" )
                print( "Please Enter a new value..!" )
                continue
            degrees.append(degree)
            i += 1
        except:
            print("Error Input!!")
    avg = sum(degrees)/SUB_NUMBER
    print(avg)
    if avg >= 85:
        print("A")
    elif avg >= 75:
        print("V.G")
    elif avg >= 65:
        print("G")
    elif avg >= 50 :
        print("Pass")
    else:
        print("Filed")

if __name__ == "__main__":
    main()
```