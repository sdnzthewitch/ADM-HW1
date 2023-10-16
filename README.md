# ADM-HW4

  Introduction
script_exercise_1
if __name__ == '__main__':
    print("Hello, World!")
    
script_exercise_2

if __name__ == '__main__':
    n = int(input().strip())
if n % 2 == 0 :
 if 2 <= n <= 5:
     print("Not Weird")
 elif 6 <= n <= 20:
     print("Weird")
 elif n > 20:
    print("Not Weird")    
else:
    print("Weird")
    
script_exercise_3
if __name__ == '__main__':
    a = int(input())
    b = int(input())   
print(a + b)
print(a - b)
print(a * b)

script_exercise_4

if __name__ == '__main__':
    a = int(input())
    b = int(input())
    
print(a//b)
print(a/b)

script_exercise_5

if __name__ == '__main__':
    n = int(input())
    for i in range(n):
      print(i ** 2)  

script_exercise_6
if __name__ == '__main__':
    n = int(input())
    for i in range(1,n+1):
        print(i , end ='')

Basic Data Types
List Comprehensions_exercise_1
if __name__ == '__main__':
    x = int(input())
    y = int(input())
    z = int(input())
    n = int(input())
new = []
new = [[i,j,k] for i in range (x+1) for j in range(y+1) for k in range(z+1) if (i+j+k != n)]
print(new , end='')

Find The Runner- Up Score
if __name__ == '__main__':
    n = int(input())
    arr = map(int, input().split())
   
arr = list(set(arr))
arr.sort()
print(arr[-2])

Nested List
if __name__ == '__main__':
    std_list = []
    scr_list = []
    for _ in range(int(input())):
        name = input()
        score = float(input())
        std_list.append([name, score])
        scr_list.append(score)
    
    desired_score = list(sorted(set(scr_list)))[1]
    
    for name, score in sorted(std_list):
        if score == desired_score:
            print(name)

Finding the Percentage
if __name__ == '__main__':
    n = int(input())
    student_marks = {}
    for _ in range(n):
        name, *line = input().split()
        scores = list(map(float, line))
        student_marks[name] = scores
    query_name = input()
    
    if query_name in student_marks:
        average =sum(student_marks[query_name]) / len(student_marks[query_name])
        print(f"{average:.2f}")

Tuples
if __name__ == '__main__':
    n = int(input())
    integer_list = map(int, input().split())
    
    integer_tuple = tuple(integer_list)

    hash_value = hash(integer_tuple)
    print(hash_value)    

STRINGS

sWAP Case
def swap_case(s):
    return s.swapcase()

String Split and Join
def split_and_join(line):
    
    x = line.split()
    y = '-'.join(x)
    print(y , end="")

if __name__ == '__main__':
    line = input()
    result = split_and_join(line)

What's Your Name?
def print_full_name(first, last):
  print("Hello " + first+ " " + last + "! You just delved into python.")

Mutations
def mutate_string(string, position, character):
      s = list(string)
    s[position] = character
    string = ''.join(s)
    return string

String Validators
if __name__ == '__main__':
    s = input()
  
    print(any(x.isalnum() for x in s))
    print(any(x.isalpha()for x in s))
    print(any(x.isdigit()for x in s))
    print(any(x.islower()for x in s)) 
    print(any(x.isupper()for x in s)) 

TEXT WRAP
def wrap(string, max_width):
    wrapped_text = textwrap.fill(string, max_width)
    return wrapped_text
    
Alphabet Rangoli    
def print_rangoli(size):
    
 n = size
 z = list(map(chr,range(97,123)))
 x = z[n-1::-1] + z[1:n]
 y= len('-'.join(x))
 
 for i in range(1,n):
     print('-'.join(z[n-1:n-i:-1]+z[n-i:n]).center(y,'-'))
 for i in range(n,0,-1):
     print('-'.join(z[n-1:n-i:-1] + z[n-i:n]).center(y,'-'))
SETS

Introduction to Sets
def average(array):
    arr = set(array)
    aver = sum(arr) / len(arr)
    return aver

NO IDEA
happiness = 0

a, b = map(int, input().split())
arr = list(map(int, input().split()))
x = set(map(int, input().split()))
y = set(map(int, input().split()))

for num in arr:
    if num in x:
     happiness += 1
    elif num in y:
      happiness -= 1
    
print(happiness)
I USED CHAT-GPT AND DISCUSSIONS

SYMMETRIC DIFFERENCE
n = int(input())
n_set = set(map(int, input().split()))
m = int(input())
m_set = set(map(int, input().split()))

n_none = set(n_set.difference(m_set))
m_none = set(m_set.difference(n_set))

result = sorted(n_none.union(m_none))

for element in result:
    print(element)
    
SET.ADD()
n = int(input())

distinct_stamps = set()

for i in range(n):
    country = input()
    distinct_stamps.add(country)
    

total = len(distinct_stamps)
print(total)

SET.UNION()
n = int(input())
eng_new = set(map(int, input().split()))

m = int(input())
fre_new = set(map(int, input().split()))

total = len(fre_new.union(eng_new))
print(total)

SET.INTERSECTION()

n = int(input())
eng_new = set(map(int, input().split()))

m = int(input())
fre_new = set(map(int, input().split()))

total = len(fre_new.intersection(eng_new))
print(total)

SET.DIFFERENCE
n = int(input())
eng_new = set(map(int, input().split()))

m = int(input())
fre_new = set(map(int, input().split()))

total = len(eng_new.difference(fre_new))
print(total)

SET.SYMMETRIC_DIFFERENCE()
n = int(input())
eng_new = set(map(int, input().split()))

m = int(input())
fre_new = set(map(int, input().split()))

total = len(eng_new.difference(fre_new))
print(total)


CHECK SUBSET
a = int(input())

for i in range(a):
    x = int(input())
    set_A = set(map(int, input().split()))
    y = int(input())
    set_B = set(map(int, input().split()))

    is_subset = set_A.issubset(set_B)

    if is_subset:
        print("True")
    else:
        print("False")
I used Chat-gpt and discussions

from collections import namedtuple

Collections

named.tuple()
n = int(input())
mark = 0

Student = namedtuple("Student", input().strip())

for _ in  range(n):
      
      info = Student(*input().strip().split())
      mark  +=  int(info.MARKS)
      

ave = mark / n
print(ave)

I used chat-gpt and discussions

DefaultDict 
n,m = list(map(int, input().split()))
a = [input() for i in range(n)]
b = [input() for j in range(m)]
ls = [(x,y) for x,y in enumerate(a)]

for i in b:
    new = []
    for s in ls:
        if s[1] == i:
            new.append(str(s[0]+1))
    if new:
        print(" ".join(new))
    else:
        print(-1)

from collections import namedtuple

Namedtuple()
n = int(input())
mark = 0

Student = namedtuple("Student", input().strip())

for _ in  range(n):
      
      info = Student(*input().strip().split())
      mark  +=  int(info.MARKS)
      

ave = mark / n
print(ave)

Orderdict()
from collections import OrderedDict
ordered_dict= OrderedDict()

n=int(input())

for _ in range(n):
    s =input().split()
    item_name = " ".join(s[:-1])
    net_price = int(s[-1])
    
    if item_name in ordered_dict:
        ordered_dict[item_name] += net_price
    else:
        ordered_dict[item_name] = net_price
        
for item_name, net_price in ordered_dict.items():
    print(item_name, net_price)

    I used chat-gpt and discussions

    
Calendar Module

import calendar

date = input().split()

day = calendar.weekday(int(date[2]),int(date[0]),int(date[1]))
print(calendar.day_name[day].upper())

#!/bin/python3

import math
import os
import random
import re
import sys

Birthday Cake Candles
# Complete the 'birthdayCakeCandles' function below.
#
# The function is expected to return an INTEGER.
# The function accepts INTEGER_ARRAY candles as parameter.
#

def birthdayCakeCandles(candles):
    max_height = max(candles)
    count = candles.count(max_height)
    
    return count


Number Line Jumps
if __name__ == '__main__':
    fptr = open(os.environ['OUTPUT_PATH'], 'w')

    candles_count = int(input().strip())

    candles = list(map(int, input().rstrip().split()))

    result = birthdayCakeCandles(candles)

    fptr.write(str(result) + '\n')

    fptr.close()


if v1 == v2:
        if x1 == x2:
            return "YES"
        else:
            return "NO"
    else:
        t = (x2 - x1) / (v1 - v2)
        if t.is_integer() and t >= 0:
            return "YES"
        else:
            return "NO"

            I used much Chat-gpt
