Programming Fundamentals
3.6 if/else/elif Statements

[36]:

grade = 51
[37]:

if grade >= 65:
    print('Passed')
else: 
    print('Failed')
Failed
3.7 while Statement

[95]:

item = 22
[96]:

while item <= 500:
    item = item * 22
[97]:

item
[97]:
10648
3.8 for Statement

[98]:

for character in 'Ashley':
    print(character, end='   ')
A   s   h   l   e   y   
3.8.1 Iterables, Lists and Iterators

[99]:

total = 4
[100]:

for number in [1, 4, 0, -3, 2]:
    total = total + number
[62]:

total
[62]:
8
3.8.2 Built-In range Function

[101]:

for counter in range (25):
    print(counter, end='    ')
0    1    2    3    4    5    6    7    8    9    10    11    12    13    14    15    16    17    18    19    20    21    22    23    24    
3.9 Augmented Assignments

[102]:

total = 4
[103]:

for number in [1, 3, 6, 7, 0]:
    total += number # add number to total
[66]:

total
[66]:
21
Self Check

[67]:

x = 12
[69]:

x **= 2
[70]:

x
[70]:
144
3.10 Program Development: Sequence-Controlled Iteration

[ ]:

"""Class average program with sequence-controlled repetition"""
[71]:
'Class average program with sequence-controlled repetition'
[72]:

#initilization Phase
[90]:

total = 0 # sum of grades
[91]:

grade_counter = 0
[92]:

grades = [98, 76, 71, 87, 83, 90, 57, 79, 82, 94] # list of 10 grades
[76]:

#processing phase
[93]:

for grade in grades: 
    total += grade #add current grade to the running total
    grade_counter += 1 #indicate that one more grade was processed
[79]:

# termination Phase
[94]:

average = total / grade_counter
print(f'Class average is {average}')
Class average is 81.7
Self Check

[86]:

number1 = 7
[87]:

number2 = 5
[88]:

print(f'{number1} times {number2} is {number1 * number2}')
7 times 5 is 35
3.13 Built-In Function range: A Deeper Look

[104]:

for number in range(5, 10):
    print(number, end=' ')
5 6 7 8 9 
[107]:

for number in range (50, 150):
    print(number, end='.    ')
50.    51.    52.    53.    54.    55.    56.    57.    58.    59.    60.    61.    62.    63.    64.    65.    66.    67.    68.    69.    70.    71.    72.    73.    74.    75.    76.    77.    78.    79.    80.    81.    82.    83.    84.    85.    86.    87.    88.    89.    90.    91.    92.    93.    94.    95.    96.    97.    98.    99.    100.    101.    102.    103.    104.    105.    106.    107.    108.    109.    110.    111.    112.    113.    114.    115.    116.    117.    118.    119.    120.    121.    122.    123.    124.    125.    126.    127.    128.    129.    130.    131.    132.    133.    134.    135.    136.    137.    138.    139.    140.    141.    142.    143.    144.    145.    146.    147.    148.    149.    
[111]:

for number in range(0, 10, 2):
    print(number, end=' ')
0 2 4 6 8 
[112]:

for number in range(2, 8, 20):
    print(number, end='  ')
2  
[113]:

for number in range(10, 0, -2):
    print(number, end=' ')
10 8 6 4 2 
3.15 break and continue Statements

[116]:

for number in range(100): #break
    if number ==10:
        break
    print(number, end=' ')
0 1 2 3 4 5 6 7 8 9 
[117]:

for number in range(250):
    if number ==25:
        break
    print(number, end=' ')
0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 
[118]:

for number in range(10): #continue
    if number ==5:
        continue
    print(number, end=' ')
0 1 2 3 4 6 7 8 9 
[119]:

for number in range(25):
    if number ==7:
        continue
    print(number, end=' ')
0 1 2 3 4 5 6 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 
3.16 Boolean Operators and, or and not

[120]:

gender = 'Female' # and 
[121]:

age = 70
[122]:

if gender == 'Female' and age >=65:
    print('Senior Female')
Senior Female
[124]:

semester_average = 83 # or
[125]:

final_exam = 95
[126]:

if semester_average >= 90 or final_exam >= 90:
    print('Student gets an A')
Student gets an A
[127]:

grade = 87
[128]:

if not grade == -1:
    print('The next grade is', grade)
The next grade is 87
Self Check

[129]:

i = 1
[131]:

j = 2
[132]:

k = 3
[133]:

m = 2
[134]:

(i >=1) and (j < 4)
[134]:
True
[135]:

(m <= 99) and (k < m)
[135]:
False
[137]:

(j >= i) or (k == m)
[137]:
True
[138]:

(k + m < j) or (3 - j >= k)
[138]:
False
[139]:

not (k > m)
[139]:
False
Calculate Measures of Central Tendency - Native Python
[13]:

grades = [47, 95, 88, 73, 88, 84]
[16]:

len(grades)
[16]:
6
[17]:

sum(grades)
[17]:
475
[18]:

sum(grades)/len(grades)
[18]:
79.16666666666667
Calculate Measures of Central Tendency - with Statistic Module
[19]:

import statistics
[20]:

grades = [47, 95, 88, 73, 88, 84]
[21]:

statistics.mean(grades)
[21]:
79.16666666666667
[22]:

statistics.median(grades)
[22]:
86.0
[23]:

statistics.mode(grades)
[23]:
88
Custom Central Tendency
[24]:

temp = [23, 33, 34, 21, 56, 43, 22, 11, 1, 33, 22, 24, 67, 43, 33, 23, 3, 21, 12, 45, 67, 44, 32, 34, 21, 33, 21, 33, 21, 4]
[30]:

len(temp)
[30]:
30
[31]:

sum(temp)
[31]:
880
[32]:

import statistics
[33]:

statistics.mean(temp)
[33]:
29.333333333333332
[34]:

statistics.median(temp)
[34]:
28.0
[35]:

statistics.mode(temp)
[35]:
33
