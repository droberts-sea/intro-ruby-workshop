@snap[midpoint span-100]

# Conditionals

@snapend

---

# TODO Agenda

---

## Learning Goals

---

## Conditionals

Sometimes we need our program to make a choice about what to do next

- Should I run these statements or not?

- Should I run these statements or those statements?

---

## Conditionals

```ruby zoom-15
puts "Enter username:"
username = gets.chomp

if username == "alovelace"
  puts "Welcome back Ada"
end

puts "Initializing user settings..."
```

**Predict and observe:**

- What if you type `alovelace`?
- What if you type `kjohnson`?

---

## Inequalities

```ruby zoom-15
spring_sales = 15 + 22 + 17

if spring_sales > 40
  puts "What a strong quarter!"
end
```

**Predict and observe**

---

## Comparing Variables

```ruby zoom-15
spring_sales = 15 + 22 + 17
summer_sales = 35 + 16 + 27

if spring_sales < summer_sales
  puts "Summer was stronger"
end
```

**Predict and observe**

---

## if - else

```ruby zoom-15
spring_sales = 15 + 22 + 17
summer_sales = 35 + 16 + 27

if spring_sales > summer_sales
  puts "Spring was stronger"
else
  puts "Summer was stronger"
end
```

**Predict and observe**

We call each path the code can take a **branch**, as in "the if branch" and "the else branch"

---

## Relational Operators

| op   | name             | 5 vs 10 | 8 vs 8 | 10 vs 5 |
| ---- | ---------------- | ------- | ------ | ------- |
| `==` | equal            | ❌      | ✅     | ❌      |
| `!=` | not equal        | ✅      | ❌     | ✅      |
| `<`  | less than        | ✅      | ❌     | ❌      |
| `<=` | less or equal    | ✅      | ✅     | ❌      |
| `>`  | greater than     | ❌      | ❌     | ✅      |
| `>=` | greater or equal | ❌      | ✅     | ✅      |

---

## Data Types

```ruby zoom-15
result = 2 + 3
```

What is the **value** of `result`?

What is the **data type** of `result`?

---

## Data Types

```ruby zoom-15
result = 2 < 3
```

What is the **value** of `result`?

What is the **data type** of `result`?

---

## Boolean Values

Ruby includes the values `true` and `false`

<p class="small">Called **Boolean** values, after George Boole</p>
<br>
Represents the results of a **comparison**

<p class="small">Like `spring_sales < 40`</p>
<br>
Can be stored in a variable like any other value

You don't see them typed out very often, but it's good to know they're there

---

## Conditional Debugging

What if we make a mistake writing our conditional and our code goes down the wrong path?

<p class="small">No error, but bad behavior</p>
<br>
How can we get more info about what went wrong?

---

## Conditional Debugging

```ruby zoom-15
spring_sales = # complex math
sales_target = # different complex math

if spring_sales > sales_target
  # we expected the program to take
  # this branch, but it didn't!
end
```

Could be the math was wrong, we've used the wrong operator, or something else

---

## Intermediate Variable

```ruby zoom-12
spring_sales = # complex math
sales_target = # different complex math

puts "spring_sales is #{spring_sales}"
puts "sales_target is #{sales_target}"

comparison = spring_sales > sales_target
puts "comparison result is ${comparison}"
if comparison
  # ...
end
```
<br>

**_"When in doubt, print it out"_**

---

## Common Mistake

```ruby zoom-15
puts "Enter username:"
username = gets.chomp

if username = "alovelace"
  puts "Welcome back Ada"
end

puts "Initializing user settings..."
```

This program always prints `Welcome back Ada`. Why?

---

## Vocab

---

## Review Questions