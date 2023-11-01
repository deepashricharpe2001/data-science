1. Write a Python program that asks the user for their age and prints "You are an adult" if the age is 18 or older, otherwise prints "You are a minor'.



```python
# input the age 
Age = int(input('what is the Age? :'))
# giving a if condition statement which is if the age is 18 or greater than 18 print given statement
if Age >= 18 :
    print('you are an adult')
# else the age is not 18 or less than 18 then print given statement 
else :
    print('You are a minor')
```

    what is the Age? :90
    you are an adult
    

2. Write a program that takes a numerical grade (out of 100) as input and prints the corresponding letter grade according to the following scale:
   
   90-100: A
    
    80-89: B
    
    70-79: C
    
    60-69: D
    
    Below 60: F



```python
# we took some numerical grade out of 100  as input 
Grade = int(input('what is grade?  :'))
# using if condition we will find the grade for perticular marks
if Grade >= 90:
    print('A') # if marks is 90 or above than that my grate will print as A 
elif(Grade >= 80):
    print('B') #if marks is 80 or above than that my grate will print as B
elif(Grade >= 70):
    print('C') #if marks is 70 or above than that my grate will print as C
elif(Grade >= 60):
    print('D')#if marks is 60 or above than that my grate will print as D
else : 
    print('F')#if marks is below than 60 then my grate will print as F

```

    what is grade?  :90
    A
    

3. Write a program that calculates the Body Mass Index (BMI) of a person. The user should input their weight in kilograms and height in meters. The program should then print whether the person is underweight, normal weight, overweight, or obese



```python
# Input weight in kilograms and height in meters
weight = float(input('what is the weight in kg ? : '))
height = float(input('what is the height in meters ? : '))
# now calculate the bmi by using bmi formula
BMI = weight / height
print(BMI)
# using conditional statement we will get to know cotegory of bmi 
if BMI <=18 :
    print('underweight')
elif 18.5<= BMI <= 24.9 :
    print('normal weight')
elif 25.0 <= BMI <= 29.5:
    print('over weight')
else :
    print('obese')
```

    what is the weight in kg ? : 70
    what is the height in meters ? : 5.9
    11.864406779661016
    underweight
    

4. Write a program that asks the user for three numbers and prints the maximum of the three.



```python
# Input three numbers from the user
num1 = float(input('Enter the first number: '))
num2 = float(input('Enter the second number: '))
num3 = float(input('Enter the third number: '))


```

5. Write a program that asks the user for a temperature (in Celsius) and prints "It's freezing" if the temperature is below 0, "It's cool" if it's between 0 and 10, "It's warm" if it's between 10 and 20, and "It's hot" if it's above 20



```python
temp = float(input(' what is temperture ? :'))

if temp <=0 : 
    print("it's freezing")
elif 0 <= temp <= 10 :
    print("its cool")
elif 10 <= temp <= 20 :
    print("its warm")
else :
    print("its hot")
```

     what is temperture ? :9
    its cool
    

6. Write a program that asks the user for a number (1-7) and prints the corresponding day of the week.



```python
day = int(input('enter the week day number : '))

if day == 1: 
    print('monday')
elif day == 2:
    print('tuesday')
elif day == 3:
    print('wednesday')
elif day == 4:
    print('thusday')
elif day == 5:
    print('friday')
elif day == 6:
    print('saturday')
elif  day == 7:
    print('sunday')
else :
    print('no day')
```

    enter the week day number : 9
    no day
    

7. Write a program that asks the user for a number and prints "In range" if the number is between 10 and 20 (inclusive), and "Out of range" otherwise.



```python
num = int(input("Enter a number: "))
if num >= 10 and num <= 20:
    print("In range")
else:
    print("Out of range")
```

    Enter a number: 90
    Out of range
    

8. Write a program that asks the user for an integer and prints whether it's even or odd.




```python
num = float(input('enter a number :'))
if num %2 ==0 : 
    
    print("even")
else :
    print("odd")
```

    enter a number :9
    odd
    


 9. Write a Python program to add 'ing' at the end of a given string (string length should be equal to or more than 3). If the given string already ends with 'ing' then add 'ly' instead.If the string length of the given string is less than 3, leave it unchanged



```python
string = str(input('enter a string : '))
if len(string)>=3:
        print(string + 'ing')
elif len(string)<=3:
    print(string+ 'ly')
else:
    print(string + 'ing')

        
```

    enter a string : j
    jly
    

10. Create rock-paper-scissors by using the if condition.



```python
import random 
b = list('rps')
random.shuffle(b)

b = b[0]
a = input('player - I :').lower()
if (a =='p' and b == 'r' ) or (a =='s' and b == 'p' ) or (a == 'r ' and b == 's'):
    print('a win')
elif a== b :
    print('tie')
else :
    print('b')
```

    player - I :p
    a win
    

12. Create a dynamic calculator which asks for numbers and operator and return the answers,
            
            
       Example
     
     Input: Type first number: 10",
   
   
     Type any of this (+, -, *, /, %, **): ,*
   
      Assignment-2 ,
    
      Type second number: 19,
     
     Output:Answer is 190



```python
num1 = float(input(" enter the first number : "))
ope = input("choose opertor: +, -, *, /, %, ** :")
num2 = float(input(" enter the secound number : "))

if ope == "+":
    print(num1+num2)
elif ope== "-":
    print(num1 - num2)
elif ope == "*":
    print(num1 * num2)
elif ope == "/":
    print(num1/num2)
elif ope == "%": 
    print(num1% num2)
elif ope == "**":
    print(num1**num2)
else :
    print(0)

```

     enter the first number : 10
    choose opertor: +, -, *, /, %, ** :*
     enter the secound number : 19
    190.0
    

12. Manoj Kumar has family and friends. Help him remind them who is who. Given a string with a name, return the relation of   that person to Manoj Kumar.,
     Person Relation,
    
   Shiva father ,Letha mother, Tarun brother,Kavitha sister ,,Strange Coder.



```python
rel = str(input(' what is the name of person : '))
if rel == 'kavita' : 
    print('sister')
elif rel == 'trun' :
    print('brother')
elif rel == 'letha':
    print('mother')
elif rel == 'shiva':
    print('father')
else :
    print('stanger code')
    
```

     what is the name of person : shiva
    father
    

12. Write a python program that takes in a word and determines whether or not it is plural. A plural word is one that ends with “s”



```python
word = str(input('write the words: '))

if word.endswith('s'):
    print('it  is plural')
else:
    print('not plural')
```

    write the words: sss
    it  is plural
    

14. A company decided to give a bonus of 5% to employees if his/her year of service is more than 5 years.Ask user for their salary and year of service and print the net bonus amount.



```python
salary = float(input("Enter  salary: "))
service = int(input("Enter years of service: "))
if service >= 5:
    bouns_percetage = 5
    bonus = (bouns_percetage / 100)*salary
    print(bonus)
    print("congoo")
else:
    print ('no bonus!!!')


```

    Enter  salary: 1888888
    Enter years of service: 4
    no bonus!!!
    

15. Take values of length and breadth of a rectangle from the user and check if it is square or not.



```python
lenght = float(input('what is lenght :'))
breadth = float(input('what is breadth : ')) 

if lenght == breadth :
    print("its a square")
else :
    print("it is rectangle ")
```

    what is lenght :4
    what is breadth : 4
    its a square
    

16. Accept any city from the user and display the momentum of the city 
    '
    Hyderabad  : “charminar”
            
      “Delhi”         : “red fort
         
     “Agra           : Taj mahal
               
       If the city name is not given correctly, give him a warning message.



```python
city = str(input("Enter a city : "))

if city == "Delhi":
    print("Red Fort")

elif city == "agra":
    print("Taj Mahal")

elif city == "Hyderabad":
    print("charminar")
else:
    print("enter the correct place")


```

    Enter a city : Hyderabad
    charminar
    


17. Write a program to check whether a person is eligible for voting or not  (voting age>=18).



```python
age = int(input(' enter your age : '))
if age >= 18 :
    print('youre eligiable for voting')
else :
    print('youre not eligiable for voting')
```

     enter your age : 88
    youre eligiable for voting
    

18. Accept three sides of the triangle and check whether the triangle is possible or not.(Triangle is possible only when the sum of any two sides is greater than 3 rd side).




```python
# there are three side of tringle a ,b,c 
a = float(input('what is lenght of first side : '))
b = float(input('what is lenght of second side : '))
c = float(input('what is lenght of third side : '))

if a+ b > c : 
    print('its triangle')
elif a+c > b:
    print('its triangle')
elif b+c > a:
    print('its triangle')
else :
    print ('its not a triagle')
```

    what is lenght of first side : 12
    what is lenght of second side : 13
    what is lenght of third side : 20
    its triangle
    


```python

```
