@snap[midpoint span-100]
# Variables and Math
@snapend

---

# TODO Agenda

---

## Learning Goals

---

## Why Math?

Computers were invented as a tool for doing math quickly and precisely

<p class="small">Specifically **calculations** or "number crunching"</p>

Humans are bad at calculating - we make mistakes!

Our job is to **direct** the computer and **check** that we told it to do the right thing

---

## Statements

A line of code that does something is called a **statement**

<p class="small">Most lines of our programs will be statements</p>

Statements are made up of a **command** and some **data**

---

## The Program So Far

```ruby zoom-20
puts "Hello World!"
```

<br>

**Command:** `puts` - print text to the screen

**Data:** `"Hello World!"` - a **string** of characters

---

## Top to Bottom

We can add **more statements** to our program

Each statement goes on a separate line

The Ruby interpreter starts at the top of the file and executes statements **one by one, in order**

```ruby zoom-20
puts "Hello World!"
puts "This gets printed too"
```

---

## Independent Runs

Each time we run our code, the Ruby interpreter **starts over from scratch**

Anything from previous runs, including deleted code and user input, will not affect the current run

This is good! It makes writing and debugging code much more straightforward.

---

## Comments

Any line that starts with a `#` is ignored by the Ruby interpreter

These are called **comments**, and are used to write notes

```ruby
# Traditional first program
puts "Hello World!"
```

---

## Tracking Data

`puts` doesn't keep track of the data it prints

If we want to print the same thing twice, we need to type it twice

```ruby zoom-20
puts "Hello World!"
puts "Hello World!"
```

That's a lot of typing, and it leaves us open to mistakes

Idea: have the program **store data**, so we can reuse it

---

## Variables

**Variables** are used to store data

We say that you **assign** a **value** to the variable

```ruby zoom-20
message = "Hello World!"

puts message
puts message
```

**Question:** What are the **command** and **data** for the above assignment statement

---

## Don't Repeat Yourself

Repetition is boring, and leads to **mistakes**

<p class="small">Remember, computers are the ones that are good at repeating things!</p>

**Reuse** parts of your program when possible

Write code in a way that is easy to reuse

<br>

Keeping code DRY is a noble goal, but don't let it get in the way of solving the problem!

---

## Reassignment

We can give a variable a new value with another assignment statement

```ruby zoom-20
message = "Hello World!"
puts message

message = "Programming is fun"
puts message
```

**Predict and observe**

Remember: the program executes top-to-bottom, so the new value won't affect code above it

---

## Interpolation

What if we want to print out a variable plus some other text?

You can use **string interpolation** to create a string that includes the value of a variable

```ruby zoom-20
name = "Ada Lovelace"
puts "Hello #{name}!"
```

**Predict and observe**

<p class="small">Note: strings defined with 'single quotes' will not interpolate</p>

---

## Practice

Take a few minutes to practice what we've covered:

- Variable assignment
- Printing a variable to the screen
- String interpolation

Questions to answer:

- Can you store an interpolated string in a variable?
- Can you use an interpolated string in another interpolation?
- What happens to the text of an interpolated string when the original variable's value changes?

---

## Numbers

Most programming languages (including Ruby) have two kinds of numbers

**Integers** like `4`, `296` and `-7`

**Floats** ("floating point") like `-347.8`, `3.14159` and `4.0`

```ruby zoom-20
age = 28
puts "I am #{age} years old"
```

---

## Math

Ruby has several **arithmetic operators**: `+`, `-`, `*`, `/`

```ruby zoom-15
donut_count = 4 * 12 # 4 dozen
attendees = 8
donuts_per_head = donut_count / attendees

puts "#{donuts_per_head} donuts each"
```

**Predict and observe**

---

## Integer Division

What happens if we change `attendees` to `7`?

```ruby zoom-15
donut_count = 4 * 12 # 4 dozen
attendees = 7
donuts_per_head = donut_count / attendees

puts "#{donuts_per_head} donuts each"
```

**Predict and observe**

What if we change it to `7.0`?

---

## Precision

When you divide two integers, any decimal will be dropped

<p class="small">We say the result is **truncated**</p>

```ruby zoom-15
puts 48 / 7
# 6
```

If at least one number is a float, the decimal is kept

<p class="small">We say that floats have more **precision** than integers</p>

```ruby zoom-15
puts 48 / 7.0
# 6.857142857142857
```

---

## Order of Operations

What will the following code print?

```ruby zoom-15
average = 3 + 5 + 7 / 3
puts average
```

<p class="fragment">It prints 10, but the average of 3, 5 and 7 is 5</p>

<p class="fragment">Multiplication and division always happen **before** addition and subtraction</p>

---

## Order of Operations

Use **parentheses** to override the default order

```ruby zoom-15
average = (3 + 5 + 7) / 3
puts average
# prints 5, as expected
```

---

## Updating a Variable

Common pattern: repeatedly updating a variable 

```ruby zoom-15
total = 0

spring_sales = 15 + 22 + 17
total = total + spring_sales

summer_sales = 35 + 16 + 27
total = total + summer sales

puts "total sales: #{total}
```

---

## Update Operators

Use `+=`, `-=`, `*=`, `/=` to do math and assign

```ruby zoom-15
total = 0

spring_sales = 15 + 22 + 17
total += spring_sales

summer_sales = 35 + 16 + 27
total += summer sales

puts "total sales: #{total}
```

---

## Question

What will the following code print?

```ruby zoom-15
donut_count = 4 * 12 # 4 dozen
attendees = 10
donuts_per_head = donut_count / atttendees

puts "#{donuts_per_head} donuts each"
```

---

## Error Messages

![](assets/images/variables-math-error-1.png)

What was the problem?

---

## Band Attendance

We now have the tools to solve part of our problem

```ruby zoom-15
member_name = "Ada"
jan_attendance = 4
feb_attendance = 3
mar_attendance = 5
```

Starting with this data, print the total number of rehearsals attended by this band member

---

## Band Attendance

```ruby zoom-15
name = "Ada"
jan_attendance = 4
feb_attendance = 3
mar_attendance = 5

total = 0
total += jan_attendance 
total += feb_attendance
total += mar_attendance
puts "#{name} has attended #{total} rehearsals"
```

---

## Vocab

---

## Review Questions