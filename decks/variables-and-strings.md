@snap[midpoint span-100]
# Variables and Strings
@snapend

---

# TODO Agenda

---

## Learning Goals

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

- Variable assignment
- Printing a variable to the screen
- String interpolation

Questions to answer:

- Can you store an interpolated string in a variable?
- Can you use an interpolated string in another interpolation?
- What happens to the text of an interpolated string when the original variable's value changes?

---

## Vocab

---

## Review Questions