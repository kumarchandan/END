# Capstone Project

Generate python source code from english descriptions
---


**1. Data Cleaning**  
The given dataset has instructions in english following it's code.

Following steps are taken to clean the given dataset:
- Removal of comments from code snippet
- Removal of extra numbers in the english instructions adjacent to '#'
- Removal of extra new lines in code snippets


**2. Model Architecture**  
Similar transformer and attention model is used which was covered in the sessions.  
The only difference is the use of pre-trained code embeddings.
![Arch](https://miro.medium.com/max/906/1*FDVDbERvzb3ZsgZlzh_KSw.png)


**3. Loss function Strategy**  
Same `CrossEntropyLoss` loss function is used without any modification


**4. Data Preparation Strategy**  
- Cleaning of dataset (using script and manual)
- Training a python code embedding


**5. Data extension Strategy**  
None


**6. Embedding Strategy**  
Python code embedding is fine-tuned on the given dataset with the help of the Gensim library


**7. Evaluation Metrics**  
Similar as covered in the sessions.

**8. Outputs**  
Example: 1
```python
input_text = 'write a function to return the perimeter of a isoscales triangle'
---
def cal_perimeter_iso_triangle(s1,s2 ) : 
     return 2*s1+s2 
```
Example: 2
```python
input_text = 'write a python function to add two numbers'
---
def add_two_numbers(num1 , num2 ) : 
     sum = num1 + num2 
     return sum 
```
Example: 3
```python
input_text = 'write a function to return the area of an ellipse'
---
def cal_area_ellipse(minor , major ) : 
     pi = 3.14 
     return pi*(minor*major ) 
```
Example: 4
```python
input_text = 'write a function to return the perimeter of an equilateral triangle'
---
def cal_perimeter_eq_triangle(a ) : 
     return 3*a 
```
Example: 5
```python
input_text = 'write a function to return the surface area of a sphere'
---
def cal_area_sphere(radius ) : 
     pi = 3.14 
     return 4*pi*(radius**2 ) 
```
Example: 6
```python
input_text = 'write a function to return the total surface area of a cylinder'
---
def cal_cylinder_volume(height , radius ) : 
     pi=3.14 
     return pi*(radius**2)*height 
```
Example: 7
```python
input_text = 'write a function to return the area of triangle by heros formula'
---
def cal_triangle_area(a : float , b : float , c : float)->float : 
     if a or b or c : 
         s = ( a+b+c)/2 
         if s > a and s > b and s > c : 
             area = ( s*(s - a)*(s - b)*(s - c))**(1/2 ) 
             return round(area,2 ) 
         else : 
             return none 
     return none 
```
Example: 8
```python
input_text = 'write a function to return the cartisian distance between two points'
---
def cal_cart_distance(x1 : float , y1 : float , x2 : float , y2 : float)->float : 
     return ( ( x1-x2)**2+(y1-y2)**2)**(1/2 ) 
```
Example: 9
```python
input_text = 'function to find fibonacci sequence'
---

 def fibonacci(n ) : 
     if n<0 : 
         print("incorrect input " ) 

     elif n==0 : 
         return 0 

     elif n==0 : 
         return 1 
     else : 
         return fibonacci(n-1)+fibonacci(n-2 ) 



 print(fibonacci(9 ) ) 
```
Example: 10
```python
input_text = 'function to validate email address using regex'
---

 import re 

 regex = ' ^[a - z0 - 9]+[\._]?[a - z0 - 9]+[@]\w+[.]\w{2,3}$ ' 
 def check(email ) : 
     if(re.search(regex , email ) ) : 
         print("valid email " ) 
     else : 
         print("invalid email " ) 
```
Example: 11
```python
input_text = 'write a function to find factorial'
---

 def factorial(n ) : 
     if n = = 1 : 
         return 1 
     else : 
         return n * factorial(n - 1 ) 
```
Example: 12
```python
input_text = 'Write a function to adds two lists element wise'
---
def sub_listelements(l1 : list , l2 : list ) : 
     return [ i+j for i , j in zip(l1,l2 ) ] 
```
Example: 13
```python
input_text = 'write a function to capitalize a string'
---

 def capitalize(s , lower_rest = false ) : 
   return ' ' .join([s[:1].upper ( ) , ( s[1:].lower ( ) if lower_rest else s[1 : ] ) ] ) 
```
Example: 14
```python
input_text = 'write a Python function to find the single number in a list that doesnt occur twice'
---
def single_number(arr ) : 
     result = 0 
     for i in arr : 
         result ^= i 
     return result 
```
Example: 15
```python
input_text = 'Write a function to return the area of a equilateral triangle'
---
def cal_eq_triangle_area(a : float)->float : 
     if a : 
         return ( 3**(1/2))*(a**2)/4 
     else : 
         return none 
```
Example: 16
```python
input_text = 'Write a program to check whether a file/path/direcory exists or not'
---
file_path = " path / here " 
 import os.path 
 os.path.exists(file_path ) 
```
Example: 17
```python
input_text = 'Write a function to find volume of a cuboid'
---
def cal_cuboid_volume(length : float , breadth : float)->float : 
     return length*breadth*height / length 
```
Example: 18
```python
input_text = 'Write a function to calculate volume of Triangular Pyramid'
---
def volumetriangular(a , b , h ) : 
     return ( 0.1666 ) * a * b * h 
```
Example: 19
```python
input_text = 'Write a python function to determine if a year is leap year or not'
---

 year = int(input("enter a year : ") ) 
 if ( year % 4 ) = = 0 : 
    if ( year % 100 ) = = 0 : 
        if ( year % 400 ) = = 0 : 
            print(f"{year } is a leap year " ) 
        else : 
            print(f"{year } is not a leap year " ) 
    else : 
        print(f"{year } is not a leap year " ) 
 else :
```
Example: 20
```python
input_text = 'Write a python function to find gcd using eucliean algorithm'
---

 def compute_gcd(x , y ) : 
     if x > y : 
         smaller = y 
     else : 
         smaller = x 
     for i in range(1,smaller + 1 ) : 
         if((x % i = = 0 ) and ( y % i = = 0 ) ) : 
             hcf = i 
     return hcf 

 num1 = 54 
 num2 = 24 

 print("the h.c.f . is " , compute_hcf(num1 , num2 ) ) 
```
Example: 21
```python
input_text = 'Write a python program to flatten  a multidimensional list'
---
mylist = [ 1 , 2 , 3 , 4 , 5 ] 
 mylist = [ i for i in mylist if i ] 
```
Example: 22
```python
input_text = 'Write a program to check whether a number is prime or not'
---

 num = 407 


 if num > 1 : 
    for i in range(2,num ) : 
        if ( num % i ) = = 0 : 
            print(num,"is not a prime number " ) 
            print(i,"times",num//i,"is",num ) 
            break 
    else : 
        print(num,"is a prime number " ) 

 else : 
    print(num,"is not a prime number " ) 
```
Example: 23
```python
input_text = 'write a program to find and print the largest among three numbers'
---

 num1 = 10 
 num2 = 12 
 num3 = 14 
 if ( num1 > = num2 ) and ( num1 > = num3 ) : 
    largest = num1 
 elif ( num2 > = num1 ) and ( num2 > = num3 ) : 
    largest = num2 
 else : 
    largest = num3 
 print(f'largest:{largest } ' ) 
```
Example: 24
```python
input_text = 'write a python function to calculate simple interest'
---
def simple_interest(p , t , r ) : 
     si = ( p * t * r)/100 
     return si 
```
Example: 25
```python
input_text = 'write a python program to print all numbers in an interval'
---
num = 12 
 for i in range(1 , 11 ) : 
    print(num , i , i , i , ' = ' , num*i ) 
```


**9. Attention graphs**  
![Attention](https://raw.githubusercontent.com/kumarchandan/END/main/week14/attention_images.png)


**10. Summary**  
The capstone project gave me an opportunity to work on a real life NLP problem and solve it from scratch. I could use most of the concepts which I learnt during the course. I could have never imagined that a transformer model with a variation of attentions can be so powerful which can solve complex NLP problems such as writing code in any programming language. Thank you so much for opening a door to an exciting world!
