@snap[midpoint span-100]

# Arrays

@snapend

---

# TODO Agenda

---

## Learning Goals

---

## Motivation

@snap[west span-60]

```ruby zoom-12
attendance_requirement = 10
name = "Ada"
jan_attendance = 4
feb_attendance = 3
mar_attendance = 5

total = 0
total += jan_attendance
total += feb_attendance
total += mar_attendance

if total < attendance_requirement
# ...
```

@snapend

@snap[east span-40 text-left]
This code could be better

Lots of **repetition**

What if we want to track **12 months** of attendance?

Using separate variables **doesn't scale**
@snapend

---

## Arrays

@snap[west span-50]
Arrays are used to store a **list** of related values

The array gets a **name**

We use **numbers** to refer to individual values

Instead of labeling individual bins, label a whole row, then put a number on each bin
@snapend

@snap[east span-50]
![](assets/images/storage-bins.jpg)
@snapend

---

## Array Syntax

Array syntax is all about **square brackets** and numbers

We call the numbers of an array **indices** (plural of index)

The first index is always **0**, then **1**, then **2**, etc.

```ruby zoom-12
# Create an array and assign it to a variable
pie_flavors = ["apple", "blueberry", "pecan"]

# Read a value
puts pie_flavors[1]
# blueberry

# Assign a value to replace "pecan"
pie_flavors[2] = "pumpkin"
```

---

## Arrays are Variables

An array is a variable, so you can do all the normal variable things

```ruby zoom-12
pie_flavors = ["apple", "blueberry", "pecan"]

puts pie_flavors

puts "The contents of the array is #{pie_flavors}"
```

**Question:** What is the syntax for an **array literal**?

---

## Variables in Arrays

You can put variables in an array, and use them as indices

<p class="small">Remember, variables and literals are interchangeable</p>

```ruby zoom-12
new_flavor = "lemon meringue"
pie_flavors = ["apple", "blueberry", "pecan", new_flavor]

index = 2
puts "Flavor at index #{index}: #{pie_flavors[index]}"
```

**Question:** What will this program print?

---

## Length

The `Array` data type has several useful methods

`.length` returns the number of elements in the array

```ruby zoom-12
pie_flavors = ["apple", "blueberry", "pecan"]

puts "We have #{pie_flavors.length} different pies"

puts pie_flavors
```

**Question:** How could you get the index of the last element in the array?

---

## Push

The `.push` method adds a value to the end of an array

<p class="small">The new value can be a literal or a variable</p>

```ruby zoom-12
pie_flavors = ["apple", "blueberry", "pecan"]

puts "What flavor should we add to our menu?"
new_flavor = gets.chomp

pie_flavors.push new_flavor
```

**Question:** What is the index of the new value?

---

## Arguments

You can't just call `.push` by itself - you need to tell it what to push

We say that `.push` takes one **argument**

<p class="small">We **pass** the **argument** into the **method** when we **call** it</p>

```ruby zoom-12
pie_flavors.push
# Produces an ArgumentError

pie_flavors.push "pumpkin"
# OK
```

**Question:** What other method have we seen that takes an argument?

---

## Empty Array

With `.push`, we can start with an empty array and add values as we go

```ruby zoom-12
pie_flavors = []
pie_flavors.push "apple"
pie_flavors.push "blueberry"
pie_flavors.push "pecan"
```

This is great for getting input from a user

**Question:** what is the length of an empty array?

---

## Practice

Write a program that uses an array and produces the following output:

```zoom-15
Please give me 3 numbers
Number:
12
Number:
5
Number:
29
Presto! 12 + 5 + 29 = 46!
```

You'll need to track both the individual numbers and their sum

<p class="small">Keep this program around, we'll come back to it</p>

---

## Out of Bounds

What will the following code print to the screen?

```ruby zoom-12
pie_flavors = ["apple", "blueberry", "pecan"]

puts "flavor: #{pie_flavors[0]}"
puts "flavor: #{pie_flavors[1]}"
puts "flavor: #{pie_flavors[2]}"
puts "flavor: #{pie_flavors[3]}"
```

---

## `nil`

`nil` is a special value that means "nothing"

If you try to read past the end of an array, you get `nil`

When you print `nil` to the screen you get nothing

<p class="small">This can make debugging tricky!</p>

You can use the `.nil?` method to check for `nil`

```ruby zoom-12
pie_flavors = ["apple", "blueberry", "pecan"]

puts "flavor 0 is nil: #{pie_flavors[0].nil?}" # false
puts "flavor 3 is nil: #{pie_flavors[3].nil?}" # true
```

---

## Vocab

| Term          | Definition                                                      |
| ------------- | --------------------------------------------------------------- |
| Array         | Variable that stores many values, accessible by number          |
| Index         | Number used to access a value from an array, always starts at 0 |
| Out of bounds | Trying to read past the end of an array                         |
| `nil`         | Special Ruby value that represents nothing                      |
| Argument  | Extra data that some methods require                      |

---

## Review Questions
