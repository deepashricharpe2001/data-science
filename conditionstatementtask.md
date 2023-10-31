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

    what is the Age? :12
    You are a minor
    

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

    what is grade?  :87
    B
    

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

    what is the weight?60
    what is the height?5.2
    11.538461538461538
    underweight
    

4. Write a program that asks the user for three numbers and prints the maximum of the three.



```python
# Input three numbers from the user
num1 = float(input('Enter the first number: '))
num2 = float(input('Enter the second number: '))
num3 = float(input('Enter the third number: '))

# Find the maximum number with the three numbers
maxnum = max(num1, num2, num3)

# Print the maximum number
print(num1, num2 , num3, maxnum)

```

    Enter the first number: 1
    Enter the second number: 2
    Enter the third number: 3
    1.0 2.0 3.0 3.0
    

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

     what is temperture ? :11
    its warm
    

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
else :
    print('sunday')
```

    enter the week day number : 5
    friday
    

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

    enter a number :3
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

    enter a string : f
    fly
    


```python

```
