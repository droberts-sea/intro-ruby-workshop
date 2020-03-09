@snap[midpoint span-100]
# Supplemental: Iteration
@snapend

---

# TODO Agenda

---

## Learning Goals

- **Use** an `.each` loop to iterate through an array
- **Use** a `.times` loop to iterate without an array
- **Define** the following terms: block, loop, iteration, iteration variable, hard-coded  

---

## Loops

The `.each` method runs some code once for every value in the array

This is called **iteration** or **looping**

```ruby zoom-12
pie_flavors = ["apple", "blueberry", "pecan"]

pie_flavors.each do |flavor|
  puts "You could order #{flavor} pie"
end
```

**Predict and observe**

---

## Blocks

```ruby zoom-12
pie_flavors = ["apple", "blueberry", "pecan"]

pie_flavors.each do |flavor|
  puts "You could order #{flavor} pie"
end
```

We call everything between `do` and `end` a **block**

The block will run 3 times

Each time the `flavor` variable will hold a different value from the array

<p class="small">We call `flavor` an **iteration variable**</p>

---

## Practice Tracker

Convert the practice tracker program to use an array instead of separate variables

For now, hard-code practice hours into the array literal

Calculate total practice hours using a loop

---

## `.times` Loops

Sometimes you need to loop without an array

Integers have a method `.times` that does just that

```ruby zoom-12
target = 100
puts "Counting to #{target}"

target.times do |i|
  puts i
end
```

**Question:** What goes in the **iteration variable** `i`?

**Question:** What are the first and last numbers printed by this program?

---

## Filling an Array

A common use of `.times` is to fill an array with data

```ruby zoom-12
squares = []

10.times do |i|
  squares.push i * i
end

puts "The first 10 square numbers: #{squares}"
```

---

## Practice Tracker

Adjust the practice tracker program to take user input in a loop

**Bonus:** allow the user to specify how many weeks of practice data to collect

---

## Practice Tracker

```ruby zoom-12
name = "Ada"
practice_log = []

puts "How many weeks of data?"
week_count = gets.chomp
week_count = week_count.to_i

week_count.times do |i|
  hours_practiced = gets.chomp
  practice_log.push hours_practiced.to_i
end

# ... sum, average, print the results ...
```

---

## Vocab: Hard-coded

When we use a literal to put our data directly in our code file, we call this **hard-coding** the data

You can also get data by

- Asking the user

- Reading a file

- Downloading it from the internet

- Generating it automatically

---

## Vocab

| Term               | Definition                                                |
| ------------------ | --------------------------------------------------------- |
| Block              | Code between `do` and `end`, usually run in a special way |
| Loop               | Block of code that runs many times                        |
| Iteration          | The act of looping                                        |
| Iteration Variable | A variable supplied to a block while looping              |
| Hard-coded         | Written as a literal directly in your code                |

---

## Review Questions

- What is the syntax for an `.each` loop?

- What are two ways we've seen to get data into your program?

- What will the following program print?

```ruby zoom-15
puts "before"

[].each do |value|
  puts "inside"
end

puts "after"
```