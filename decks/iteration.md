@snap[midpoint span-100]

# Iteration

@snapend

---

# TODO Agenda

---

## Learning Goals

---

## Iteration

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

<!-- TODO consider a .times slide, could do without but it's directly relevant to the application -->
<!-- ## .times -->

---

## Vocab

| Term      | Definition                                                |
| --------- | --------------------------------------------------------- |
| Block     | Code between `do` and `end`, usually run in a special way |
| Loop      | Block of code that runs many times                        |
| Iteration | The act of looping                                        |

---

## Review Questions
