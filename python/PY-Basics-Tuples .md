<h1>Tuples in Python</h1>

<p><strong>Welcome!</strong> Here you will learn about the tuples in the Python Programming Language. By the end of this lab, you'll know the basics tuple operations in Python, including indexing, slicing and sorting.</p> 

<hr>

<h2 id="tuple">Tuples</h2>

In Python, there are different data types: string, integer and float. These data types can all be contained in a tuple as follows:

Now, let us create your first tuple with string, integer and float.


```python
# Create your first tuple

tuple1 = ("disco",10,1.2 )
tuple1
```

The type of variable is a **tuple**. 


```python
# Print the type of the tuple you created

type(tuple1)
```

<h3 id="index">Indexing</h3>

 Each element of a tuple can be accessed via an index. The following table represents the relationship between the index and the items in the tuple. Each element can be obtained by the name of the tuple followed by a square bracket with the index number:

We can print out each value in the tuple:


```python
# Print the variable on each index

print(tuple1[0])
print(tuple1[1])
print(tuple1[2])
```

We can also use negative indexing. We use the same table above with corresponding negative values:

We can obtain the last element as follows (this time we will not use the print statement to display the values):


```python
# Use negative index to get the value of the last element

tuple1[-1]
```

We can display the next two elements as follows:


```python
# Use negative index to get the value of the second last element

tuple1[-2]
```


```python
# Use negative index to get the value of the third last element

tuple1[-3]
```

<h3 id="concate">Concatenate Tuples</h3>

We can concatenate or combine tuples by using the **+** sign:


```python
# Concatenate two tuples

tuple2 = tuple1 + ("hard rock", 10)
tuple2
```

We can slice tuples obtaining multiple values as demonstrated by the figure below:

<h3 id="slice">Slicing</h3>

We can slice tuples, obtaining new tuples with the corresponding elements: 


```python
# Slice from index 0 to index 2

tuple2[0:3]
```

We can obtain the last two elements of the tuple:


```python
# Slice from index 3 to index 4

tuple2[3:5]
```

We can obtain the length of a tuple using the length command: 


```python
# Get the length of tuple

len(tuple2)
```

This figure shows the number of elements:

<h3 id="sort">Sorting</h3>

 Consider the following tuple:


```python
# A sample tuple

Ratings = (0, 9, 6, 5, 10, 8, 9, 6, 2)
```

We can sort the values in a tuple and save it to a new tuple: 


```python
# Sort the tuple

RatingsSorted = sorted(Ratings)
RatingsSorted
```

<h3 id="nest">Nested Tuple</h3>

A tuple can contain another tuple as well as other more complex data types. This process is called 'nesting'. Consider the following tuple with several elements: 


```python
# Create a nest tuple

NestedT =(1, 2, ("pop", "rock") ,(3,4),("disco",(1,2)))
```

Each element in the tuple including other tuples can be obtained via an index as shown in the figure:


```python
# Print element on each index

print("Element 0 of Tuple: ", NestedT[0])
print("Element 1 of Tuple: ", NestedT[1])
print("Element 2 of Tuple: ", NestedT[2])
print("Element 3 of Tuple: ", NestedT[3])
print("Element 4 of Tuple: ", NestedT[4])
```

We can use the second index to access other tuples as demonstrated in the figure:

 We can access the nested tuples :


```python
# Print element on each index, including nest indexes

print("Element 2, 0 of Tuple: ",   NestedT[2][0])
print("Element 2, 1 of Tuple: ",   NestedT[2][1])
print("Element 3, 0 of Tuple: ",   NestedT[3][0])
print("Element 3, 1 of Tuple: ",   NestedT[3][1])
print("Element 4, 0 of Tuple: ",   NestedT[4][0])
print("Element 4, 1 of Tuple: ",   NestedT[4][1])
```

We can access strings in the second nested tuples using a third index:


```python
# Print the first element in the second nested tuples

NestedT[2][1][0]
```


```python
# Print the second element in the second nested tuples

NestedT[2][1][1]
```

 We can use a tree to visualise the process. Each new index corresponds to a deeper level in the tree:

Similarly, we can access elements nested deeper in the tree with a fourth index:


```python
# Print the first element in the second nested tuples

NestedT[4][1][0]
```


```python
# Print the second element in the second nested tuples

NestedT[4][1][1]
```

The following figure shows the relationship of the tree and the element <code>NestedT[4][1][1]</code>:

<h2 id="quiz">Quiz on Tuples</h2>

Consider the following tuple:


```python
# sample tuple

genres_tuple = ("pop", "rock", "soul", "hard rock", "soft rock", \
                "R&B", "progressive rock", "disco") 
genres_tuple
```

Find the length of the tuple, <code>genres_tuple</code>:


```python
# Write your code below and press Shift+Enter to execute
len(genres_tuple)
```

Double-click __here__ for the solution.

<!-- Your answer is below:
len(genres_tuple)
-->

Access the element, with respect to index 3: 


```python
# Write your code below and press Shift+Enter to execute
genres_tuple[3]
```

Double-click __here__ for the solution.

<!-- Your answer is below:
genres_tuple[3]
-->

Use slicing to obtain indexes 3, 4 and 5:


```python
# Write your code below and press Shift+Enter to execute
genres_tuple[3:6]
```

Find the first two elements of the tuple <code>genres_tuple</code>:


```python
# Write your code below and press Shift+Enter to execute
genres_tuple[0:2]

```


```python
# Write your code below and press Shift+Enter to execute
genres_tuple.index("disco")
```

Generate a sorted List from the Tuple <code>C_tuple=(-5, 1, -3)</code>:


```python
# Write your code below and press Shift+Enter to execute
C_tuple = (-5,1,-3)
C_tuple1 = sorted(C_tuple)
print(C_tuple1)
```
