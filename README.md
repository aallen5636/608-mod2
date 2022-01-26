Programming Fundamentals
3.6 if/else/elif Statements

grade = 51
if grade >= 65:
    print('Passed')
else: 
    print('Failed')
Failed

3.7 while Statement

item = 22
while item <= 500:
    item = item * 22
item
10648

3.8 for Statement

for character in 'Ashley':
    print(character, end='   ')
A   s   h   l   e   y

3.8.1 Iterables, Lists and Iterators

total = 4
for number in [1, 4, 0, -3, 2]:
    total = total + number
total
8

3.8.2 Built-In range Function

for counter in range (25):
    print(counter, end='    ')
0    1    2    3    4    5    6    7    8    9    10    11    12    13    14    15    16    17    18    19    20    21    22    23    24    

3.9 Augmented Assignments

total = 4
[103]:
for number in [1, 3, 6, 7, 0]:
    total += number # add number to total
total
21

Self Check

x = 12
x **= 2
x
144

3.10 Program Development: Sequence-Controlled Iteration

"""Class average program with sequence-controlled repetition"""
'Class average program with sequence-controlled repetition'

#initilization Phase
total = 0 # sum of grades
grade_counter = 0
grades = [98, 76, 71, 87, 83, 90, 57, 79, 82, 94] # list of 10 grades

#processing phase
for grade in grades: 
    total += grade #add current grade to the running total
    grade_counter += 1 #indicate that one more grade was processed

# termination Phase
average = total / grade_counter
print(f'Class average is {average}')
Class average is 81.7

Self Check
number1 = 7
number2 = 5
print(f'{number1} times {number2} is {number1 * number2}')
7 times 5 is 35

3.13 Built-In Function range: A Deeper Look

for number in range(5, 10):
    print(number, end=' ')
5 6 7 8 9 

for number in range (50, 150):
    print(number, end='.    ')
50.    51.    52.    53.    54.    55.    56.    57.    58.    59.    60.    61.    62.    63.    64.    65.    66.    67.    68.    69.    70.    71.    72.    73.    74.    75.    76.    77.    78.    79.    80.    81.    82.    83.    84.    85.    86.    87.    88.    89.    90.    91.    92.    93.    94.    95.    96.    97.    98.    99.    100.    101.    102.    103.    104.    105.    106.    107.    108.    109.    110.    111.    112.    113.    114.    115.    116.    117.    118.    119.    120.    121.    122.    123.    124.    125.    126.    127.    128.    129.    130.    131.    132.    133.    134.    135.    136.    137.    138.    139.    140.    141.    142.    143.    144.    145.    146.    147.    148.    149.    

for number in range(0, 10, 2):
    print(number, end=' ')
0 2 4 6 8 

for number in range(2, 8, 20):
    print(number, end='  ')
2  

for number in range(10, 0, -2):
    print(number, end=' ')
10 8 6 4 2 
3.15 break and continue Statements

for number in range(100): #break
    if number ==10:
        break
    print(number, end=' ')
0 1 2 3 4 5 6 7 8 9 

for number in range(250):
    if number ==25:
        break
    print(number, end=' ')
0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 

for number in range(10): #continue
    if number ==5:
        continue
    print(number, end=' ')
0 1 2 3 4 6 7 8 9 

for number in range(25):
    if number ==7:
        continue
    print(number, end=' ')
0 1 2 3 4 5 6 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 

3.16 Boolean Operators and, or and not

gender = 'Female' # and 
age = 70
if gender == 'Female' and age >=65:
    print('Senior Female')
Senior Female

semester_average = 83 # or
final_exam = 95
if semester_average >= 90 or final_exam >= 90:
    print('Student gets an A')
Student gets an A

grade = 87
if not grade == -1:
    print('The next grade is', grade)
The next grade is 87

Self Check

i = 1
j = 2
k = 3
m = 2
(i >=1) and (j < 4)
True
(m <= 99) and (k < m)
False
(j >= i) or (k == m)
True
(k + m < j) or (3 - j >= k)
False
not (k > m)
False
Calculate Measures of Central Tendency - Native Python

grades = [47, 95, 88, 73, 88, 84]
len(grades)
6
sum(grades)
475
sum(grades)/len(grades)
79.16666666666667

Calculate Measures of Central Tendency - with Statistic Module

import statistics
grades = [47, 95, 88, 73, 88, 84]
statistics.mean(grades)
79.16666666666667
statistics.median(grades)
86.0
statistics.mode(grades)
88
Custom Central Tendency
temp = [23, 33, 34, 21, 56, 43, 22, 11, 1, 33, 22, 24, 67, 43, 33, 23, 3, 21, 12, 45, 67, 44, 32, 34, 21, 33, 21, 33, 21, 4]
len(temp)
30
sum(temp)
880

import statistics
statistics.mean(temp)
29.333333333333332
statistics.median(temp)
28.0
statistics.mode(temp)
33
