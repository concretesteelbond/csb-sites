<h1>Lists in Python</h1>

<p><strong>Welcome!</strong> This notebook will teach you about the lists in the Python Programming Language. By the end of this lab, you'll know the basics list operations in Python, including indexing, list operations and copy/clone list.</p> 

<h3 id="index">Indexing</h3>

We are going to take a look at lists in Python. A list is a sequenced collection of different objects such as integers, strings, and other lists as well. The address of each element within a list is called an <b>index</b>. An index is used to access and refer to items within a list.

 To create a list, type the list within square brackets <b>[ ]</b>, with your content inside the parenthesis and separated by commas. Let’s try it!


```python
# Create a list

L = ["Michael Jackson", 10.1, 1982]
L
```




    ['Michael Jackson', 10.1, 1982]



We can use negative and regular indexing with a list :


```python
# Print the elements on each index

print('the same element using negative and positive indexing:\n Postive:',L[0],
'\n Negative:' , L[-3]  )
print('the same element using negative and positive indexing:\n Postive:',L[1],
'\n Negative:' , L[-2]  )
print('the same element using negative and positive indexing:\n Postive:',L[2],
'\n Negative:' , L[-1]  )
```

    the same element using negative and positive indexing:
     Postive: Michael Jackson 
     Negative: Michael Jackson
    the same element using negative and positive indexing:
     Postive: 10.1 
     Negative: 10.1
    the same element using negative and positive indexing:
     Postive: 1982 
     Negative: 1982
    

<h3 id="content">List Content</h3>

Lists can contain strings, floats, and integers. We can nest other lists, and we can also nest tuples and other data structures. The same indexing conventions apply for nesting:    



```python
# Sample List

["Michael Jackson", 10.1, 1982, [1, 2], ("A", 1)]
```




    ['Michael Jackson', 10.1, 1982, [1, 2], ('A', 1)]



<h3 id="op">List Operations</h3>

 We can also perform slicing in lists. For example, if we want the last two elements, we use the following command:


```python
# Sample List

L = ["Michael Jackson", 10.1,1982,"MJ",1]
L
```




    ['Michael Jackson', 10.1, 1982, 'MJ', 1]




```python
# List slicing

L[3:5]
```




    ['MJ', 1]



We can use the method <code>extend</code> to add new elements to the list:


```python
# Use extend to add elements to list

L = [ "Michael Jackson", 10.2]
L.extend(['pop', 10])
L
```




    ['Michael Jackson', 10.2, 'pop', 10]



Another similar method is <code>append</code>. If we apply <code>append</code> instead of <code>extend</code>, we add one element to the list:


```python
# Use append to add elements to list

L = [ "Michael Jackson", 10.2]
L.append(['pop', 10])
L
```




    ['Michael Jackson', 10.2, ['pop', 10]]



 Each time we apply a method, the list changes. If we apply <code>extend</code> we add two new elements to the list. The list <code>L</code> is then modified by adding two new elements:


```python
# Use extend to add elements to list

L = [ "Michael Jackson", 10.2]
L.extend(['pop', 10])
L
```




    ['Michael Jackson', 10.2, 'pop', 10]



If we append the list  <code>['a','b']</code> we have one new element consisting of a nested list:


```python
# Use append to add elements to list

L.append(['a','b'])
L
```




    ['Michael Jackson', 10.2, 'pop', 10, ['a', 'b']]



As lists are mutable, we can change them. For example, we can change the first element as follows:


```python
# Change the element based on the index

A = ["disco", 10, 1.2]
print('Before change:', A)
A[0] = 'hard rock'
print('After change:', A)
```

    Before change: ['disco', 10, 1.2]
    After change: ['hard rock', 10, 1.2]
    

 We can also delete an element of a list using the <code>del</code> command:


```python
# Delete the element based on the index

print('Before change:', A)
del(A[0])
print('After change:', A)
```

    Before change: ['hard rock', 10, 1.2]
    After change: [10, 1.2]
    

We can convert a string to a list using <code>split</code>.  For example, the method <code>split</code> translates every group of characters separated by a space into an element in a list:


```python
# Split the string, default is by space

'hard rock'.split()
```




    ['hard', 'rock']



We can use the split function to separate strings on a specific character. We pass the character we would like to split on into the argument, which in this case is a comma.  The result is a list, and each element corresponds to a set of characters that have been separated by a comma: 


```python
# Split the string by comma

'A,B,C,D'.split(',')
```




    ['A', 'B', 'C', 'D']



<h3 id="co">Copy and Clone List</h3>

When we set one variable <b>B</b> equal to <b>A</b>; both <b>A</b> and <b>B</b> are referencing the same list in memory:


```python
# Copy (copy by reference) the list A

A = ["hard rock", 10, 1.2]
B = A
print('A:', A)
print('B:', B)
```

    A: ['hard rock', 10, 1.2]
    B: ['hard rock', 10, 1.2]
    

Initially, the value of the first element in <b>B</b> is set as hard rock. If we change the first element in <b>A</b> to <b>banana</b>, we get an unexpected side effect.  As <b>A</b> and <b>B</b> are referencing the same list, if we change list <b>A</b>, then list <b>B</b> also changes. If we check the first element of <b>B</b> we get banana instead of hard rock:


```python
# Examine the copy by reference

print('B[0]:', B[0])
A[0] = "banana"
print('B[0]:', B[0])
```

    B[0]: hard rock
    B[0]: banana
    

This is demonstrated in the following figure: 

You can clone list  **A** by using  the following syntax:


```python
# Clone (clone by value) the list A

B = A[:]
B
```




    ['banana', 10, 1.2]



 Variable **B** references a new copy or clone of the original list; this is demonstrated in the following figure:

Now if you change <b>A</b>, <b>B</b> will not change: 


```python
print('B[0]:', B[0])
A[0] = "hard rock"
print('B[0]:', B[0])
```

    B[0]: banana
    B[0]: banana
    

<h2 id="quiz">Quiz on List</h2>

Create a list <code>a_list</code>, with the following elements <code>1</code>, <code>hello</code>, <code>[1,2,3]</code> and <code>True</code>. 


```python
# Write your code below and press Shift+Enter to execute
a_list=[1,"hello",{1,2,3},"True"]
a_list
```




    [1, 'hello', {1, 2, 3}, 'True']



Find the value stored at index 1 of <code>a_list</code>.


```python
# Write your code below and press Shift+Enter to execute
a_list[1]
```




    'hello'



Retrieve the elements stored at index 1, 2 and 3 of <code>a_list</code>.


```python
# Write your code below and press Shift+Enter to execute
a_list[1:4]
```




    ['hello', {1, 2, 3}, 'True']



Concatenate the following lists <code>A = [1, 'a']</code> and <code>B = [2, 1, 'd']</code>:


```python
# Write your code below and press Shift+Enter to execute
A=[1,'a']
B=[2,1,'d']
A+B

```




    [1, 'a', 2, 1, 'd']


