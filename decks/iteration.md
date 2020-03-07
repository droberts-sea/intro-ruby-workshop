@snap[midpoint span-100]

# Iteration

@snapend

---

# TODO Agenda

---

## Learning Goals

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

## Band Attendance

Convert the band attendance program to use an array instead of separate variables

For now, hard-code attendance numbers into the array literal

Calculate total rehearsal attendance using a loop

---

## Band Attendance

```ruby zoom-12
name = "Ada"
attendance = [4, 3, 2]
attendance_requirement = 10

total = 0
attendance.each do |month|
  total += month
end

if total < attendance_requirement
  puts "#{name} has attended too few rehearsals (#{total})"
else
  puts "#{name} has attended enough rehearsals (#{total})"
end
```

<!--

## Pattern: Max

TODO: consider adding this. Could be a 20-30 minute session by itself without serious scaffolding, but is quite valuable for thinking about iteration
 -->

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

## Band Attendance

Adjust the band attendance program to take user input in a loop

**Bonus:** allow the user to specify how many months of attendance data to collect

---

## Band Attendance

```ruby zoom-12
name = "Ada"
attendance_requirement = 10
attendance = []

puts "How many months of data?"
month_count = gets.chomp
month_count = month_count.to_i

month_count.times do |i|
  rehearsals_attended = gets.chomp
  attendance.push rehearsals_attended.to_i
end

# ... sum attendance, print the results ...
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
