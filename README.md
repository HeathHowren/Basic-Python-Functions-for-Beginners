
# Basic Python Functions

I developed most of the functions for an intro to Python course, so they aren't too complex. I wanted to publish them so others can learn from the code, and so I can easily go back to reference my old work. Enjoy!

#### Triangle Test
```python
def Validate(sideA, sideB, sideC):
    # determing if the 3 sides are capable of making a triangle
    if (((sideA + sideB) >= sideC) and ((sideB + sideC) >= sideA) and ((sideC + sideA) >= sideB)):
        return True
    else:
        return False
```
#### Triangle Area
```python
def ComputeArea(sideA, sideB, sideC): # mathmatically determing area of the tirangle
    sidesAverage = (sideA + sideB + sideC)/2
    return ((sidesAverage*(sidesAverage-sideA)*(sidesAverage-sideB)*(sidesAverage-sideC))**0.5)
```
#### Smallest Triangle Side
```python
def findMin(sideA, sideB, sideC):
    # determining which length is the smallest
    if (sideA <= sideB and sideB <= sideC):
        return sideA
    elif (sideB <= sideA and sideA <= sideC):
        return sideB
    else: 
        return sideC
```
#### Largest Trianlge Side
```python
def findMax(sideA, sideB, sideC):
    # determining which length is the largest
    if (sideA >= sideB and sideB >= sideC):
        return sideA
    elif (sideB >= sideA and sideA >= sideC):
        return sideB
    else: 
        return sideC
```
#### USD ($) to Euro (€)
```python
def UsdtoEuro(lst): # function that will convert the price from USD to Euro
    Euro = []
    for i in range(len(lst)):
        Euro.append((lst[i] * 0.85))
    return Euro
```
#### Print List Items (in special formatting)
```python
def PrintInfo(lst1, lst2): # function that will print the information of the two lists
    for i in range(len(lst1)):
        print(f"\t{lst1[i]}\t\t{lst2[i]:.2f}")
```
#### Average Value of a List
```python
def Average(lst): # function that will compute the average of the list
    sum = 0
    for i in lst:
        sum += i
    return sum/len(lst)
```
#### Convert Steps to Miles
```python
def StepsToMiles(lst):
    miles_walked = []
    for i in range(len(lst)):
        miles_walked.append(lst[i] * (1/2000))
    return miles_walked
```
#### Computing a Factorial
```python
def Factorial(numInput): # function for computing factorials of an input
    factorialNum = 0
    for i in range(numInput, 0, -1):
        factorialNum += i
    return factorialNum
```
#### Print Odd Numbers Only
```python
def SumOdds(num1, num2): # function for printing the odd numbers of a given range
    # assume n1 <= n2
    sum = 0
    for i in range(num1, num2+1):
        if (i % 2) != 0:
            print(i)
            sum += i
    print(f"The sum of the odd numbers is {sum}\n")
```
#### Priting Inverse Numbers Only
```python
def SumInverse(num1, num2): # function for printing the inverse number of a given range
    # assume n1 <= n2
    sum = 0
    for i in range(num1, num2+1):
        sum += 1/i
        print(f"1 / {i}")
    print(f"The sum of the inverse of the numbers between n1 and n2 is {sum:.2f}\n")
```
### Count Chars in String
```python
def FindChar(inputChar, inputString): # function for computing the amount of chars in a given string
    sum = 0
    for i in (inputString).lower():
        if i == (inputChar).lower():
         sum += 1
    return sum
```
### Apply (hardcoded) Discount to List
```python
def discount(lst): # defining the discount function take 30% off the total
    update = []
    for i in range(len(lst)):
        update.append((lst[i] - (lst[i] * 0.30))) # adding each item to the new list after discount rate is applied
    return update
```
