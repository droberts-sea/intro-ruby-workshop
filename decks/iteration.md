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

**Question:** What goes in the variable `i`?

**Question:** What are the first and last numbers printed by this program?

---

## Filling an Array

A common use of `.times` is to fill an array with user data

Rewrite your number-adder program from before to take user input in a loop

```zoom-15
Please give me 3 numbers
Number:
12
# ... two more numbers ...
Presto! 12 + 5 + 29 = 46!
```

**Bonus:** allow the user to specify how many numbers

<p class="small">How will you print the last line?</p>

---

## Vocab

| Term      | Definition                                                |
| --------- | --------------------------------------------------------- |
| Block     | Code between `do` and `end`, usually run in a special way |
| Loop      | Block of code that runs many times                        |
| Iteration | The act of looping                                        |

---

## Review Questions
