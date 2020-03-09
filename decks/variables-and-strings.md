@snap[midpoint span-100]
# Variables and Strings
@snapend

---

## Agenda

@snap[west span-50]

9:00  - Intro

9:20  - Hello World

9:50  - **Break**

<span style="color: #EF654A">10:00 - Variables + Strings</span>

11:00 - **Break**

@snapend

@snap[east span-50 text-left]

11:10 - Numbers + Math

11:50 - **Break**

12:00 - Conditionals

12:30 - **Done!**

@snapend

---

## Learning Goals

By the end of this module, students will be able to...

- **Describe** how the Ruby interpreter runs a program
- **Use** literals to supply values to a program
- **Use** variables to store values
- **Describe** the syntax for calling a method
- **Define** the following terms: syntax, statement, comment, value, data type, literal, variable, assignment, method, call, return

---

## Statements

A line of code that does something is called a **statement**

<p class="small">Most lines of our programs will be statements</p>

Statements are made up of an **action** and some **data**

---

## The Program So Far

```ruby zoom-20
puts "Hello World!"
```

<br>

**Action:** `puts` - print text to the screen

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

## Vocab: Syntax

"What characters do I need to type to make this part of the language work?"

Knowledge that answers this question is called **syntax**

**Question:** What is the syntax of a `puts` statement?

---

## Comments

Any line that starts with a `#` is ignored by the Ruby interpreter

These are called **comments**, and are used to write notes

```ruby
# Traditional first program
puts "Hello World!"
```

If you select some code in `repl.it`, you can turn it into a comment by pressing `cmd+/`

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

**Question:** What are the **action** and **data** for the above assignment statement?

---

## Variables

@snap[west span-50]
You can think of variables like bins on a shelf
<br>
Each bin has a label
<br>
Each bin holds one thing at a time
@snapend

@snap[east span-50]
![](assets/images/storage-bins.jpg)
@snapend

---

## Vocab: Literal

A **literal** is when you type a value directly into your code

<p class="small">The code uses **literally** this value</p>

```ruby zoom-15
# "hello" is a literal
puts "hello"

# "world" is also a literal
message = "world"
puts message
```

Variables and literals are **interchangeable**. Anywhere you can use one you can use the other as well.

---

## Vocab: Value

A **value** is one piece of data used by a program

Anything you could print to the screen is a value

So far, our program can get values from variables and literals

---

## Reassignment

We can give a variable a new value with another assignment statement

```ruby zoom-15
message = "Hello World!"
puts message

message = "Programming is fun"
puts message
```

**Predict and observe**

Remember: the program executes top-to-bottom, so the new value won't affect code above it

---

## Independent Runs

Each time we run our code, the Ruby interpreter **starts over from scratch**

Anything from previous runs, including deleted code and user input, will not affect the current run

This is good! It makes writing and debugging code much more straightforward.

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

<ul class="small">
<li>Variable assignment</li>
<li>Printing a variable to the screen</li>
<li>String interpolation</li>
</ul>

Questions to answer:

<ul class="small">
<li>Can you store an interpolated string in a variable?</li>
<li>Can you use an interpolated string in another interpolation?</li>
<li>What happens to the text of an interpolated string when the original variable's value changes?</li>
</ul>

---

## Data Types

Every value in Ruby has a **data type**

```ruby zoom-15
message = "Hello World!"
```

<p class="small">The variable `message` has the data type `String`</p>
<br>
This is also sometimes called its **class**

```ruby zoom-15
puts message.class
# String
```

---

## Methods

Every data type has related actions called **methods**

For example, the `String` data type has an `upcase` method

We can **call** (run) the method on a variable using a dot (`.`)

```ruby zoom-15
message = "hello world!"
puts message.upcase
# HELLO WORLD!
```

---

## Return Values

Many methods will **return** a value when they're finished running

**Question:** What does the `upcase` method return?

```ruby zoom-15
message = "hello world!"
puts message.upcase
# HELLO WORLD!
```

<p class="fragment">**Question:** Can you store the return value in a variable?</p>
<p class="fragment">**Question:** Did calling `message.upcase` change the original `message`? How could you find out?</p>

---

## User Input

You can get input from the user with the method `gets.chomp`

```ruby zoom-15
puts "Please enter your name"

name = gets.chomp
puts "Hello #{name}"
```

<p class="small">`gets.chomp` isn't attached to a variable, and the syntax is a little weird, but it's still a method</p>

**Question:** What does `gets.chomp` **return**?

<p class="fragment">**Question:** The statement `name = gets.chomp` contains two **actions**! What are they, and what **data** do they take?</p>

---

## Vocab

| Term      | Definition                                                                         |
| --------- | ---------------------------------------------------------------------------------- |
| Syntax    | Specific characters to type to make Ruby do a certain thing                        |
| Statement | A line of code that does something                                                 |
| Comment   | A line of code beginning with `#`, ignored by the Ruby interpreter, used for notes |
| Value     | A piece of data for the program to use                                             |
| Data Type | The category of data for a value, like `String`                                    |

---

| Term       | Definition                                                      |
| ---------- | --------------------------------------------------------------- |
| Literal    | A value typed directly into the code                            |
| Variable   | A value that is given a name and stored for later               |
| Assignment | Putting a value into a variable                                 |
| Method     | A named action the program can take                             |
| Call       | Running a method                                                |
| Return     | A method giving a value back to your program when it's finished |

---

## Review Questions

- What is the **syntax** for **string interpolation**?

- What are 3 different ways your code can get a value?

- Imagine we learn about a new piece of Ruby. The example code shows how to use it with a **literal**. Can you use it with a **variable** too?