@snap[midpoint span-100]
# Numbers and Math
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

<p class="fragment">What if we change it to `7.0`?</p>

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
total = total + summer_sales

puts "total sales: #{total}"
```

---

## Update Operators

Use `+=`, `-=`, `*=`, `/=` to both do math and assign

```ruby zoom-15
total = 0

spring_sales = 15 + 22 + 17
total += spring_sales

summer_sales = 35 + 16 + 27
total += summer_sales

puts "total sales: #{total}"
```

---

## `3` and `"3"`

What will the following code print?

```ruby zoom-15
total = 0

puts "Spring sales:"
spring_sales = gets.chomp
total += spring_sales

puts "Summer sales:"
summer_sales = gets.chomp
total += summer_sales

puts "total sales: #{total}"
```

---

## `3` and `"3"`

`gets.chomp` always gives you a `String`

It might be a string representing a number, like `"3"`

To convert a string to a number, use the method `.to_i`

---

## Converting Strings

```ruby zoom-12
total = 0

puts "Spring sales:"
input = gets.chomp
spring_sales = input.to_i
total += spring_sales

puts "Summer sales:"
input = gets.chomp
summer_sales = input.to_i
total += summer_sales

puts "total sales: #{total}"
```

**Question:** What does `.to_i` return if you type `word`?

---

<!-- TODO: should this be moved to the variables-and-strings section? -->

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

If you have time, upgrade it to get data via `gets.chomp`

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