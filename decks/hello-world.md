@snap[midpoint span-100]

# Hello World

@snapend

---

## Agenda

@snap[west span-50]

9:00  - Intro

<span style="color: #EF654A">9:20  - Hello World</span>

9:50  - **Break**

10:00 - Variables + Strings

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

- **Use** repl.it to run Ruby code in the browser
- **Compare** human skills and computer skills
- **Describe** the steps to breaking down a programming problem
- **Describe** the running problem for this workshop

---

## What is Programming?

@snap[midpoint span-100 fragment text-left]

### Programming is the art of telling a computer what to do

<br>

Computers are very good at following instructions

Computers cannot tell when they've been given the wrong instructions
@snapend

---

## Humans + Computers

@snap[west span-48]

### Human Skills

- Finding **patterns**
- Making **decisions**
- Designing
- Interpreting
- Handling **novel** situations
- Creating from nothing
- Humor, tragedy, love

@snapend

@snap[east span-48 text-left]

### Computer Skills

- Complex **calculations**
- Handling large amounts of **data**
- Following specific **rules**
- Doing the same thing over and over again
- Scaling up

@snapend

---

## repl.it

Website that allows us to quickly write and run Ruby code in the browser

Does (almost) everything the command line can do

Eliminates complex setup

Perfect for a short workshop like this

---

## Hello World!

Our first program will be as simple as possible: print the text `Hello World!` to the console

In the middle pane of repl.it, add the following code:

```ruby zoom-15
puts "Hello World!"
```

Click the green `run` button and your program's output should appear on the right

<span class="small">Keeping it simple allows us to make sure we've got everything set up correctly. Even today, when I start a new project I often write a Hello World program first to check the setup.</span>

---

## The Ruby Interpreter

Every time we press the `run` button, `repl.it` gives our code to a program called the **Ruby interpreter**

The Ruby interpreter **compiles** our code into a series of instructions the computer can understand

It then **runs** the compiled code

<p class="small">We'll talk more about the Ruby interpreter later</p>

---

## Workflow

@snap[west span-47]

### TODO IMAGE

@snapend

@snap[east span-47 text-left]
Change `World` to your name

**Predict** how this will affect the output of the program

Run the program and **observe** the results
@snapend

---

## Following Along

Should you be following along, typing out the code that appears on the screen?

Depends on your style, but probably not

Taking notes is likely more valuable

If I want you to run something, I'll say **predict & observe**

There will be explicit moments to pause and practice

---

## Workspace Setup

Have two repl.it tabs open

- One for scratch work and practice

- One for the running project we'll be building as we go along

You should have a link to these slides in your email - it might be helpful to have them open in a tab

---

## Workshop Project

As a musician, I would like to track my practice hours

- Know if I've been practicing enough

- Reward myself if I have a really good week

I would like to write a program that helps me keep track of this information, so that I can see progress toward goals and compare this week to a typical week

<br>

**Question:** Does this project leverage the strengths of computers (and humans) well?

---

## Ideal Program

**Input:** File containing daily practice data, including total time and exercises and songs covered, for everyone in my band

**Output:** Summary of this week's practice, progress toward goals

<br>

<div class="fragment">
<p>This is a lot! Way too much to start out!</p>
<p>Let's find things to cut</p>
</div>

---

## Breaking Down the Problem

Make sure you understand the problem (re-read it!)

<p class="small">**Ask questions!** What information is missing?</p>

Identify inputs and outputs

Solve by hand first

Find an easier version of the same problem

<p class="small">Solve for one before you solve for many</p>

---

## Starting Point

**Input:** Number of hours practiced per week for several weeks

**Output:** Comparison of this week's hours to previous weeks

Once we have this working we can start to think about more features

---

## Solve By Hand

| Member    | Week 1 | Week 2 | Week 3 |
| --------- | ------ | ------ | ------ |
| Ada       | 4      | 3      | 5      |
| Grace     | 2      | 4      | 2      |
| Katherine | 3      | 5      | 4      |

<br>

Which members practiced more hours than average in week 3?

How do you know?

<p class="fragment">Katherine is an **edge-case** - she had exactly average practice time in week 3</p>

---

## Review Questions

- What is programming?

- What sorts of problems are computers good at solving?

- What are some techniques for breaking down a problem?

- How do you run code in `repl.it`?
