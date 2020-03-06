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

We call the numbers of an array **indexes**

Indexes always start at **0**

```ruby zoom-12
# Create an array and assign it to a variable
pie_flavors = ["apple", "blueberry", "pecan"]

# Read a value
puts pie_flavors[1]
# blueberry

# Assign a value
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

---



---

## Vocab

---

## Review Questions