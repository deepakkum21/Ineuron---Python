# Q1:- Install Jupyter notebook and run the first program and share the screenshot of the output


```
first_name = input('Enter your first name: ')
last_name = input('Enter your last name: ')
print('Entered name is {1} {0}'.format(first_name, last_name))
```

    Enter your first name: deepak
    Enter your last name: kumar
    Entered name is kumar deepak
    

![title](img\q1.png)

#  Q2:- Write a program which will find all such numbers which are divisible by 7 but are not a multiple of 5, between 2000 and 3200 (both included). The numbers obtained should be printed in a comma-separated sequence on a single line.


```
ans = []
for i in range(2000,3201):
    if i % 7 == 0 and i %5 !=0:
        ans.append(i)
        
print(ans)
```

    [2002, 2009, 2016, 2023, 2037, 2044, 2051, 2058, 2072, 2079, 2086, 2093, 2107, 2114, 2121, 2128, 2142, 2149, 2156, 2163, 2177, 2184, 2191, 2198, 2212, 2219, 2226, 2233, 2247, 2254, 2261, 2268, 2282, 2289, 2296, 2303, 2317, 2324, 2331, 2338, 2352, 2359, 2366, 2373, 2387, 2394, 2401, 2408, 2422, 2429, 2436, 2443, 2457, 2464, 2471, 2478, 2492, 2499, 2506, 2513, 2527, 2534, 2541, 2548, 2562, 2569, 2576, 2583, 2597, 2604, 2611, 2618, 2632, 2639, 2646, 2653, 2667, 2674, 2681, 2688, 2702, 2709, 2716, 2723, 2737, 2744, 2751, 2758, 2772, 2779, 2786, 2793, 2807, 2814, 2821, 2828, 2842, 2849, 2856, 2863, 2877, 2884, 2891, 2898, 2912, 2919, 2926, 2933, 2947, 2954, 2961, 2968, 2982, 2989, 2996, 3003, 3017, 3024, 3031, 3038, 3052, 3059, 3066, 3073, 3087, 3094, 3101, 3108, 3122, 3129, 3136, 3143, 3157, 3164, 3171, 3178, 3192, 3199]
    


```
ans = [i for i in range(2000,3201) if i % 7 == 0 and i %5 !=0]
print(ans)
```

    [2002, 2009, 2016, 2023, 2037, 2044, 2051, 2058, 2072, 2079, 2086, 2093, 2107, 2114, 2121, 2128, 2142, 2149, 2156, 2163, 2177, 2184, 2191, 2198, 2212, 2219, 2226, 2233, 2247, 2254, 2261, 2268, 2282, 2289, 2296, 2303, 2317, 2324, 2331, 2338, 2352, 2359, 2366, 2373, 2387, 2394, 2401, 2408, 2422, 2429, 2436, 2443, 2457, 2464, 2471, 2478, 2492, 2499, 2506, 2513, 2527, 2534, 2541, 2548, 2562, 2569, 2576, 2583, 2597, 2604, 2611, 2618, 2632, 2639, 2646, 2653, 2667, 2674, 2681, 2688, 2702, 2709, 2716, 2723, 2737, 2744, 2751, 2758, 2772, 2779, 2786, 2793, 2807, 2814, 2821, 2828, 2842, 2849, 2856, 2863, 2877, 2884, 2891, 2898, 2912, 2919, 2926, 2933, 2947, 2954, 2961, 2968, 2982, 2989, 2996, 3003, 3017, 3024, 3031, 3038, 3052, 3059, 3066, 3073, 3087, 3094, 3101, 3108, 3122, 3129, 3136, 3143, 3157, 3164, 3171, 3178, 3192, 3199]
    

![q2](img\q2.png)

# Q3:- Write a Python program to accept the user's first and last name and then getting them printed in the the reverse order with a space between first name and last name


```
first_name = input('Enter your first name: ')
last_name = input('Enter your last name: ')
print('{1} {0}'.format(first_name, last_name))

user_name = input('Enter your name: ')
name = user_name.split()    
last_name, first_name = name[0], name[len(name)-1]
print('{} {}'.format(first_name, last_name))
```

    Enter your first name: deepak
    Enter your last name: kumar
    kumar deepak
    Enter your name: deepak kumar singh
    singh deepak
    

![q3](img\q3.png)

# Q4:- Write a Python program to find the volume of a sphere with diameter 12 cm.
# Formula: V=4/3 * π * r 3


```
import math
def sphere_volume(diameter):
    radius = diameter/2
    return 4/3 * math.pi * radius * radius * radius

vol = sphere_volume(12)
print('the volume of sphere with diameter {} cm is {vol:.2f} cm cube'.format( 12, vol=vol))
```

    the volume of sphere with diameter 12 cm is 904.78 cm cube
    

![q4](img\q4.png)

# Q5:- Write a program which accepts a sequence of comma-separated numbers from console and generate a list.


```
comma_separated_numbers = input('Enter comma-separated numbers: ')
num_list_string = comma_separated_numbers.split(',')
num_list = []
for i in num_list_string:
    if len(i) != 0:
        num_list.append(int(i))
num_list
```

    Enter comma-separated numbers: 4,4,5,6,,,62,4,,2
    




    [4, 4, 5, 6, 62, 4, 2]



![q5](img\q5.png)

# Q6:- Create the below pattern using nested for loop in Python

## *
## * *
## * * *
## * * * *
## * * * * *
## * * * *
## * * *
## * *
## *


```
for i in range(0, 5):
    for j in range(0, i + 1):
        print("*", end=' ')
    print("\r")

for i in range(5, 0, -1):
    for j in range(0, i - 1):
        print("*", end=' ')
    print("\r")
```

    * 
    * * 
    * * * 
    * * * * 
    * * * * * 
    * * * * 
    * * * 
    * * 
    * 
    



```
for i in range(0, 5):
    print("* " * (i+1), end=' ')
    print("\r")

for i in range(3, -1, -1):
    print("* " * (i+1), end=' ')
    print("\r")
```

    *  
    * *  
    * * *  
    * * * *  
    * * * * *  
    * * * *  
    * * *  
    * *  
    *  


![q6](img\q6.png)

# Q7:- Write a Python program to reverse a word after accepting the input from the user.



```
input_text = input()
input_text[::-1]
```

    abcde
    




    'edcba'



![q7](img\q7.png)

# Q8:- Write a Python Program to print the given string in the format specified in the ​sample output.
## Sample input:- 
    WE, THE PEOPLE OF INDIA, having solemnly resolved to constitute India into a 
    SOVEREIGN, SOCIALIST, SECULAR, DEMOCRATIC REPUBLIC and to secure to all 
    its citizens
    
    
## Sample output:-
WE, THE PEOPLE OF INDIA,
      having solemnly resolved to constitute India into a SOVEREIGN, !
            SOCIALIST, SECULAR, DEMOCRATIC REPUBLIC
             and to secure to all its citizens


```
print('WE, THE PEOPLE OF INDIA,')
print(f'{"": <5} having solemnly resolved to constitute India into a SOVEREIGN,', end=' !\n')
print(f'{"": <11} SOCIALIST, SECULAR, DEMOCRATIC REPUBLIC')
print(f'{"": <12} and to secure to all its citizens')
```

    WE, THE PEOPLE OF INDIA,
          having solemnly resolved to constitute India into a SOVEREIGN, !
                SOCIALIST, SECULAR, DEMOCRATIC REPUBLIC
                 and to secure to all its citizens
    

![q8](img\q8.png)


```

```
