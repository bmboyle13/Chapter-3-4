## Chapter 4 List cont. and Tuple


```python
# days=[]
days=list()
type(days)
```




    list




```python
days.append("Monday")
days.append("Tuesday")
days.append("Wednesday")
days.append("Thursday")
days.append("Friday")
```


```python
days
```




    ['Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday']




```python
days[1]
```




    'Tuesday'



### Looping through a List


```python
days
```




    ['Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday']




```python
#for Loop
for i in days: #i is a local variable which access one element at a time
    print(i)
```

    Monday
    Tuesday
    Wednesday
    Thursday
    Friday



```python
#missing a :
#for i in days
    #print(i)
```


```python
#forget indent
#for i in days:
#print(i)
```


```python

```

### Create a numerical list using `range()` function


```python
for value in range(0,10): #10 total values starting at zero
    print(value)
```

    0
    1
    2
    3
    4
    5
    6
    7
    8
    9



```python
for value in range(3,15,2): #start, stop, every other one
    print(value)
    
print("The final value is",value) #prints the final value
```

    3
    5
    7
    9
    11
    13
    The final value is 13



```python

```

## Practice 1: Think of at least five different foods that you liked a lot.
- Store the names of these foods in a list, and then use a for loop to print out the name of each food with a statement about each food, such as I love to eat `the food` .
- Add a line at the end of your program you could print a sentence such as I am a big foodie!!


```python
foods=[]
```


```python
foods.append("sushi")
foods.append("tacos")
foods.append("apples")
foods.append("chicken")
foods.append("watermellon")
foods
```




    ['sushi', 'tacos', 'apples', 'chicken', 'watermellon']




```python
for i in foods:
    print("I like to eat", i)
print("I am a big foodie")
```

    I like to eat sushi
    I like to eat tacos
    I like to eat apples
    I like to eat chicken
    I like to eat watermellon
    I am a big foodie



```python

```

### Practice 2: Print all of the odd numbers between 1 to 10 and cube each numbers and append those to a new list


```python
cube=[]
for i in range(1,10,2):
    #print("The odd numbers:",i)
    cube.append(i**3)
    #print(cube)
print("The final list is", cube)
```

    The final list is [1, 27, 125, 343, 729]



```python

```


```python

```

### Simple Statistics with a List of Numbers and strings
- min
- max
- sum


```python
numbers=[10,23,100,45,2,12]
print('Minimum Number is:', min(numbers))
print("The maximum numebr is:",max(numbers))
print("The addition of numbers is", sum(numbers))
```

    Minimum Number is: 2
    The maximum numebr is: 100
    The addition of numbers is 192



```python
#the avarage of this list
print("The avarage is:", sum(numbers)/len(numbers))
```

    The avarage is: 32.0


![image.png](attachment:image.png)


```python
names=["ani", "Ritcha", "Sam","paul", "ashley"]
```


```python
min(names) #R has dec value of 82
```




    'Ritcha'




```python
max(names)
```




    'paul'




```python
names=["ani", "Ritcha", "Sam","Paul", "ashley"]
```


```python
min(names) #P is 80
```




    'Paul'




```python
max(names)
```




    'ashley'




```python

```

### List Comprehensions


```python
#create a list pf numbers between 3 and 15 of step size 3
#find the power of 3/cube and append to a new list
cube=[]
for i in range(3,15,3):
   # print("The numbers are",i)
    cube.append(i**3)
    #print("The cube of numbers are", cube)
print("The final list is:", cube)
```

    The final list is: [27, 216, 729, 1728]



```python
cube1=[(i**3)for i in range(3,15,3)]
print(cube1)
```

    [27, 216, 729, 1728]


### Using List Comprehension: Use a for loop to print the square of numbers from 1 to 10, inclusive.


```python
square=[i**2 for i in range(1,11)]
print(square)
```

    [1, 4, 9, 16, 25, 36, 49, 64, 81, 100]



```python

```

### Using List Comprehension: Use a for loop to print the numbers from 5 to 20, inclusive.


```python
for i in range(5,21):
    print(i)
```

    5
    6
    7
    8
    9
    10
    11
    12
    13
    14
    15
    16
    17
    18
    19
    20



```python
numbers=[i for i in range(5,21)]
print(numbers)
```

    [5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20]


### Threes: Make a list of the multiples of 3 from 3 to 30. Use a for loop to print the numbers in your list.


```python
threes=[i for i in range(3,30,3)]
print(threes)
```

    [3, 6, 9, 12, 15, 18, 21, 24, 27]



```python

```


```python

```

### Make a list of the numbers from one to 10000,
- use min() and max() to make sure your list actually starts at one and ends at 10000. 
- Also, use the sum() function to see how quickly Python can add 10000 numbers.


```python
numbers=[i for i in range(1,10000)]
print("min",min(numbers))
print("max",max(numbers))
print("sum",sum(numbers))
print("Average", sum(numbers)/len(numbers))
```

    min 1
    max 9999
    sum 49995000
    Average 5000.0



```python

```


```python

```


```python

```

### Looping through a string slice


```python
players=["Charles","Martina","Michael","Eli","Florence"]
print("First three players from the list are:")

for name in players[:3]:
    print(name)
```

    First three players from the list are:
    Charles
    Martina
    Michael



```python
print("Print Martina from the list:")
for name in players[1:2]:
    print(name)
```

    Print Martina from the list:
    Martina



```python
players
```




    ['Charles', 'Martina', 'Michael', 'Eli', 'Florence']




```python
print("Michael and Eli")
for name in players[2:4]:
    print(name.lower())
```

    Michael and Eli
    michael
    eli


### Copying a list


```python
my_fav_food=["Pizza","Brownies","Chicken Fries"]
#friends_fav_food=my_fav_food     #not working for copy
friends_fav_food=my_fav_food[:]

my_fav_food.append("Ice Cream")
friends_fav_food.append("Chocolate")
```


```python
print("My Food",my_fav_food)
print("Friends food",friends_fav_food)
```

    My Food ['Pizza', 'Brownies', 'Chicken Fries', 'Ice Cream']
    Friends food ['Pizza', 'Brownies', 'Chicken Fries', 'Chocolate']



```python

```

## Nested List


## x2 = [10, ['new', 300, [3.141, 20],  345 ], 'day' ]

### Print 10 from the list


```python
x2 = [10, ['new', 300, [3.141, 20], 345 ], 'day' ]
```


```python
x2[0]
```




    10




```python
x2[1]
```




    ['new', 300, [3.141, 20], 345]




```python
x2[2]
```




    'day'



### Print 'new' from the list


```python
x2 = [10, ['new', 300, [3.141, 20], 345 ], 'day' ]

```


```python
x2[1][0]
```




    'new'



### Print 345 from the list


```python
x2 = [10, ['new', 300, [3.141, 20], 345 ], 'day' ]
```


```python
x2[1][3]
```




    345



### Print 20 from the list


```python
x2[1][2][1]
```




    20




```python
#300
x2[1][1]
```




    300



##  Tuples
### Creating Tuples
* To create an empty tuple, use empty parentheses.

Sometimes you’ll want to create a list of items that cannot
change. Tuples allow you to do just that. Python refers to values that cannot
change as immutable, and an immutable list is called a tuple.


```python
data_tuple=()
type(data_tuple)
```




    tuple




```python
data_tup=tuple()
type(data_tup)
```




    tuple




```python
names_list=["Tom","John","Rex","Paul"]
type(names_list)
```




    list




```python
#update tom to sam
names_list[0]="Sam"
print(names_list)
```

    ['Sam', 'John', 'Rex', 'Paul']



```python
#converting the list to a tuple
names_tuple=tuple([names_list])
```


```python
print(names_tuple)
type(names_tuple)
```

    (['Tom', 'John', 'Rex', 'Paul'],)





    tuple




```python
names_tuple1=("Tom","John","Rex","Paul")
print(names_tuple1)
```

    ('Tom', 'John', 'Rex', 'Paul')



```python
names_tuple1[0]="Sam"
#tuple item assignment not possible. tuple called immutable, list is mutable
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    /var/folders/5n/xr01gjrn7rv5gs_sjffmxmzc0000gn/T/ipykernel_83790/392049585.py in <module>
    ----> 1 names_tuple1[0]="Sam"
          2 #tuple item assignment not possible. tuple called immutable, list is mutable


    TypeError: 'tuple' object does not support item assignment



```python

```

### Looping Through All Values in a Tuple


```python
names_tuple1
```




    ('Tom', 'John', 'Rex', 'Paul')




```python
for name in names_tuple1: #looping through tuple is same as looping through list
    print(name)
```

    Tom
    John
    Rex
    Paul



```python

```

### Writing over a Tuple
Although you can’t modify a tuple, you can assign a new value to a variable
that holds a tuple.


```python
dimensions=(200,50)
print("....Original Dimension....")
for dim in dimensions:
    print(dim)
    
dimensions=(400,500)
print("****Modified Dimension****")
for dim in dimensions:
    print(dim)
```

    ....Original Dimension....
    200
    50
    ****Modified Dimension****
    400
    500



```python

```

### Unpacking
Unpacking is a nice way to be able to pull data out of a tuple and assign each element to an individual variable.


```python
data1=("John",1964,"Beatles")
data1[0]
```




    'John'




```python
data1[1]
```




    1964




```python
name, year, band=data1
print("Name:", name)
print("Year:", year)
print("Band:",band)
```

    Name: John
    Year: 1964
    Band: Beatles


### Lists of tuples (and tuples with lists in them).


```python
Beatles=[("John",1964,"Beatles"),
         ("Paul",1964,"Beatles"),
         ("George",1964,"Beatles"),
         ("Ringo",1964,"Beatles")]
```


```python
Beatles
```




    [('John', 1964, 'Beatles'),
     ('Paul', 1964, 'Beatles'),
     ('George', 1964, 'Beatles'),
     ('Ringo', 1964, 'Beatles')]




```python
Beatles[2][0] #[row][colum] always start with 0
```




    'George'




```python
Beatles[3][0]
```




    'Ringo'



#### Tuple unpacking fom List


```python
name, year, band=Beatles[1]
print("Name:",name)
```

    Name: Paul



```python
print("Band:",band)
```

    Band: Beatles



```python

```

Using indices, we can pull out any entry in the "table"

### Tuple concatnation with list


```python
name=("Bellarmine","University","Surf")
address=[2001, "Newburg rd", "KY",40205]
print(type(name))
print(type(address))
```

    <class 'tuple'>
    <class 'list'>



```python
list(name)+address #to make a tuple a list
```




    ['Bellarmine', 'University', 'Surf', 2001, 'Newburg rd', 'KY', 40205]




```python
name+tuple(address) #convert to a tuple
```




    ('Bellarmine', 'University', 'Surf', 2001, 'Newburg rd', 'KY', 40205)




```python

```
