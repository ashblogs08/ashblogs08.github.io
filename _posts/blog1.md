# Sequences and Iteration

***Takeaway :***

Understand the basics of a few python data types - lists, strings, tuples - as well as a control structure - for loops. By the end of this week, you will be able to write more complex programs that create drawings by incorporating for loops. Finally, we will present the basics of an accumulation pattern to you, which will be expanded on in each week for the rest of the course.

There are two ways to change an object after its been creating.

- Make a copy of the original and modify it.
- Modify the original object , which is called **mutation.**

Lists , Tuples , Strings are types of **sequences** because they are a ***collection*** and has an ***order.***

### **Will learn :**

- How mutation of existing objects works
- Recognizing the potential confusion that that can cause.
- Should be able to identify whether an object is mutable or immutable
- Should be able to identify whether a method **mutates** an object or creates a modified copy of it
- Able to recognize when two different variables are aliases for the same object.
- Predict whether an operation on one of those variables is going to cause an impact on the contents of the other one.

## Strings :

Strings are sequence or collection of characters. String is simply some characters inside quotes. Strings are ordered and while indexing whitespace matters. We cannot concatenate string and integer because of different data types.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/3c5f5eb5-430d-4a05-accd-c6a092d6989d/Screenshot_2020-06-12_at_7.57.58_PM.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/3c5f5eb5-430d-4a05-accd-c6a092d6989d/Screenshot_2020-06-12_at_7.57.58_PM.png)

Here we have to type cast like ,

```python
s = '5'
print(int(s) + 10)
```

### 

## Lists :

A list is a sequential collection of Python data values, where each value is identified by an index. The values that make up a list are called its elements. Lists are similar to strings, which are ordered collections of characters, except that the elements of a list can have any type and for any one list, the items can be of different types.

```python
[10, 20, 30, 40]
["spam", "bungee", "swallow"]
```

## Tuples :

A tuple, like a list, is a sequence of items of any type. The printed representation of a tuple is a comma-separated sequence of values, enclosed in parentheses. In other words, the representation is just like lists, except with parentheses () instead of square brackets [].

```python
julia = ("Julia", "Roberts", 1967, "Duplicity", 2009,
 "Actress", "Atlanta, Georgia")
```

### Difference between Lists and Tuples :

The key difference between lists and tuples is that a tuple is immutable, meaning that its contents can’t be changed after the tuple is created.

### The Index Operator :

We can do either Negative or Positive Indexing as in the picture below.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/503a2435-d83e-42aa-8089-4aa0dd0bf15c/Screenshot_2020-06-13_at_7.01.16_AM.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/503a2435-d83e-42aa-8089-4aa0dd0bf15c/Screenshot_2020-06-13_at_7.01.16_AM.png)

Indexing 

```python
s = 'Python'
s[0] #  positive indexing
s[-1] #  negative indexing
```

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/b0748018-7ce5-4653-83c5-526a9b73ad61/Screenshot_2020-06-13_at_7.34.44_AM.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/b0748018-7ce5-4653-83c5-526a9b73ad61/Screenshot_2020-06-13_at_7.34.44_AM.png)

Finding a mid character or element in list or string : 

```python
fruit = "grape"
midchar = fruit[len(fruit)//2]
# the value of midchar is "a"
```

### Slicing :

A ***substring of a string*** is called a slice. Selecting a slice is similar to selecting a character:

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/48dc9119-fd14-4fde-ac42-564737673d78/Screenshot_2020-06-13_at_11.15.46_AM.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/48dc9119-fd14-4fde-ac42-564737673d78/Screenshot_2020-06-13_at_11.15.46_AM.png)

The ***slice*** operator `[n:m]` returns the part of the string starting with the character at index n and go up to but not including the character at index m. Or with normal counting from 1, this is the (n+1)st character up to and including the mth character.

Slice operation can be used on tuples , strings as well as lists

Below we sliced from tuple and concatenated with another.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a573f266-f507-4989-a770-2b2aae5da805/Screenshot_2020-06-13_at_11.18.04_AM.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a573f266-f507-4989-a770-2b2aae5da805/Screenshot_2020-06-13_at_11.18.04_AM.png)

### Concatenation and Repetition :

Again, as with strings, the `+` operator concatenates lists. Similarly, the `*` operator repeats the items in a list a given number of times.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/40509c2e-1f76-4879-95f4-6dc4f10da0f0/Screenshot_2020-06-13_at_12.01.26_PM.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/40509c2e-1f76-4879-95f4-6dc4f10da0f0/Screenshot_2020-06-13_at_12.01.26_PM.png)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/9f995c6c-0860-45d7-ad7a-f57fa7a2b379/Screenshot_2020-06-13_at_12.02.38_PM.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/9f995c6c-0860-45d7-ad7a-f57fa7a2b379/Screenshot_2020-06-13_at_12.02.38_PM.png)

We cant concatenate together different types of Datatypes together. 

Repetition of a list or a string , 

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/19576579-e9f2-4793-90cc-4d5ccc1654cd/Screenshot_2020-06-13_at_12.05.02_PM.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/19576579-e9f2-4793-90cc-4d5ccc1654cd/Screenshot_2020-06-13_at_12.05.02_PM.png)

### Count and Index :

it requires that you provide one argument, which is what you would like to count. The method then returns the number of times that the argument occured in the string/list the method was used on.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6593876d-b8c7-41f1-9982-6f5c19c07c09/Screenshot_2020-06-13_at_1.07.16_PM.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6593876d-b8c7-41f1-9982-6f5c19c07c09/Screenshot_2020-06-13_at_1.07.16_PM.png)

Count method on string

Count is case sensitive there is difference between ***'We' and 'we'***

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/7b16a328-c22e-42c7-a00a-032d917d794b/Screenshot_2020-06-13_at_1.08.12_PM.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/7b16a328-c22e-42c7-a00a-032d917d794b/Screenshot_2020-06-13_at_1.08.12_PM.png)

Count method on list

The other method that can be helpful for both `strings` and `lists` is the `index` method. The `index` method requires one argument, and, like the `count` method, it takes only `strings` when index is used on strings, and any type when it is used on l`ists`. For both `strings` and `lists`, `index` returns the leftmost index where the argument is found. If it is unable to find the argument in the `string` or `list,` then an error will occur.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e9d88f18-2a6b-41f5-933e-a71ab5db8617/Screenshot_2020-06-13_at_1.14.27_PM.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e9d88f18-2a6b-41f5-933e-a71ab5db8617/Screenshot_2020-06-13_at_1.14.27_PM.png)

Index on Lists and Strings

We will get a Runtime Error if we try to find a thing which isnt in the list or tuple 

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/3f8b8e25-85b0-4277-ab29-36378a83cbd9/Screenshot_2020-06-13_at_12.26.07_PM.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/3f8b8e25-85b0-4277-ab29-36378a83cbd9/Screenshot_2020-06-13_at_12.26.07_PM.png)

### Split and Join :

Splitting a string or lists can be done by using this syntax `.split()` after the variable you want to split add the method this will return a list of split words.

If we didnt gave any argument to the split it will split the element along white space and returns them as a list.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c6184bf8-578a-46e4-b44d-89d7ff53dff4/Screenshot_2020-06-13_at_2.15.49_PM.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c6184bf8-578a-46e4-b44d-89d7ff53dff4/Screenshot_2020-06-13_at_2.15.49_PM.png)

If we split with an given argument in below example 'e' it will split along the character 'e' wherever it detect a 'e' it will split along it.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6fc135df-8c18-4b69-aa32-24d8724ec373/Screenshot_2020-06-13_at_2.18.18_PM.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6fc135df-8c18-4b69-aa32-24d8724ec373/Screenshot_2020-06-13_at_2.18.18_PM.png)

Likewise we split we can even join lists or strings , for example like below we want to join the list with '/' so it picks out the ',' and puts in '/' between them and join it.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e3bf6f4e-e805-48d0-9cb1-2d69d0b12a59/Screenshot_2020-06-13_at_2.24.31_PM.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e3bf6f4e-e805-48d0-9cb1-2d69d0b12a59/Screenshot_2020-06-13_at_2.24.31_PM.png)

From a string we split and turn them into a list.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/db852126-44a9-4250-999d-576ae7c2208a/Screenshot_2020-06-13_at_2.30.07_PM.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/db852126-44a9-4250-999d-576ae7c2208a/Screenshot_2020-06-13_at_2.30.07_PM.png)

## Iteration :

The basic building of a program is to make it efficient rather typing the code each time we can iterate them to save time and thats the efficient way of doing things in programming. 

Whether it is updating the bank balances of millions of customers each night, or sending email messages to thousands of people programming involves instructing the computer to do many repetitive actions.

We call this ***iteration ,** real word example we use **iteration***

- Displaying a list of friends on SnapChat
- Updating the position of every character on the screen of a video game
- Displaying the locations that Doctors Without Borders operates in.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/59237e89-9794-4fd4-8598-8af723a1fbb1/Screenshot_2020-06-14_at_10.36.48_AM.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/59237e89-9794-4fd4-8598-8af723a1fbb1/Screenshot_2020-06-14_at_10.36.48_AM.png)

For Loop 

For loop is one type of iteration which iterate over sequences until the end of the loop given.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/2ddefe3d-c8d4-456d-9c5d-c2c4f1748d1d/Screenshot_2020-06-14_at_10.40.40_AM.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/2ddefe3d-c8d4-456d-9c5d-c2c4f1748d1d/Screenshot_2020-06-14_at_10.40.40_AM.png)

Structure of for loop

For loop iterating over strings.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/531b3b87-417b-4188-88ef-92ee80c89f32/Screenshot_2020-06-14_at_10.42.47_AM.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/531b3b87-417b-4188-88ef-92ee80c89f32/Screenshot_2020-06-14_at_10.42.47_AM.png)

The loop variable `achar` is automatically reassigned each character in the string “Go Spot Go”. We will refer to this type of sequence iteration as ***iteration by item***. Note that the for loop processes the characters in a string or items in a sequence one at a time from left to right.

Traversal means accessing each and every element present in a data structure like an array or a linked list etc.

It doesnt matter we give string or integer as a sequence to iterate over it will iterate based on how many items are present. 

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/566b3c1f-c52d-4cb5-99d2-bb0268b5787f/Screenshot_2020-06-14_at_10.56.20_AM.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/566b3c1f-c52d-4cb5-99d2-bb0268b5787f/Screenshot_2020-06-14_at_10.56.20_AM.png)

### Accumulator Pattern:

The accumulator pattern is a common programming pattern where you iterate through the contents of a list, and you accumulate a single value, such as the sum of all of the items in that list.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6dc55ec7-c929-4b51-adc4-30fed559388a/Screenshot_2020-06-14_at_11.00.55_AM.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6dc55ec7-c929-4b51-adc4-30fed559388a/Screenshot_2020-06-14_at_11.00.55_AM.png)

**The anatomy of the accumulation pattern includes:**

1. **initialising** an “accumulator” variable to an initial value (such as 0 if accumulating a sum)**i**
2. i**terating** (e.g., traversing the items in a sequence)
3. **updating** the accumulator variable on each iteration (i.e., when processing each item in the sequence)

### Range Function :

The range function gives out a sequence depends upon the number of desired range we give.

Range function doesnt give a list, it gives values to iterate over. To change range() to a list we can do ,

```python
print(list(range(10))
# Will cast range to list
```

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/fef40f30-1b55-409f-b18e-b0707180b3cb/Screenshot_2020-06-14_at_11.19.11_AM.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/fef40f30-1b55-409f-b18e-b0707180b3cb/Screenshot_2020-06-14_at_11.19.11_AM.png)

One important thing to know about the range function in python3 is that if we want to use it outside of ***iteration***, we have to cast it as a list using `list()`.

if we really want to print the indexes (positions) along with the fruit names, then iterating through the indexes as in the previous versions is available to us. Python also provides an enumerate function which provides a more “pythonic” way of enumerating the items in a list.

# The Way of Programmer:

### Naming a variable for loop:

When we define a name of iterate variable make it singular noun of the sequence variable which was defined with plural noun. So by this way we will know exactly what we are doing.  For example below,

1. Use singular nouns for the iterator variable, which is also called the loop variable (things like “song”, “book”, “post”, “letter”, “word”).
2. Use plural nouns for the sequence variable (things like “songs”, “books”, “posts”, “letters”, “words”).

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/f7b39901-f811-4136-ae9b-3f7aeaea7a74/Screenshot_2020-06-14_at_12.47.34_PM.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/f7b39901-f811-4136-ae9b-3f7aeaea7a74/Screenshot_2020-06-14_at_12.47.34_PM.png)

### Printing Intermediate results :

To keep track of how our loop is performing and we thought of one output instead it gives a wrong one. To debug this we did the below things to print certain things to know what actually those accumulator pattern and the num in the iterate variable does.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/ecdb0d30-e226-4be1-9d6a-52e13d7bfd25/Screenshot_2020-06-14_at_12.53.20_PM.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/ecdb0d30-e226-4be1-9d6a-52e13d7bfd25/Screenshot_2020-06-14_at_12.53.20_PM.png)

Or we can do something like this to be more precise with what we are doing.  Here we added some print statements with more directions of things are going. This is one way to debug what's went wrong in our for loop code.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/b403b1da-41a5-4ec6-a9ce-16e351214803/Screenshot_2020-06-14_at_12.56.00_PM.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/b403b1da-41a5-4ec6-a9ce-16e351214803/Screenshot_2020-06-14_at_12.56.00_PM.png)

### Keeping Track of Your Iterator Variable and Your Iterable:

Iterate variable : The variable we are using to iterate through.

Iterable : The variable we want to iterate through whether it can be a list , tuples , string or any other sequences.

The iterable is the object that you will parsing through in a for loop. Generally, this object does not change while the for loop is being executed.

The iterator (loop) variable is the variable which stores a portion of the iterable when the for loop is being executed. Each time the loop iterates, the value of the iterator variable will change to a different portion of the iterable.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/507a5eb4-f577-46aa-9576-472e2b2fc938/Screenshot_2020-06-14_at_1.14.01_PM.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/507a5eb4-f577-46aa-9576-472e2b2fc938/Screenshot_2020-06-14_at_1.14.01_PM.png)
