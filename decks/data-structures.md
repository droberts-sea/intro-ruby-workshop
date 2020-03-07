@snap[midpoint span-100]

# Data Structures

@snapend

---

# TODO Agenda

---

## Learning Goals

---

## Hash or Array?

Determine whether you would use an array or a hash to store each of these collections and why.

1. The types of tea you have in your cupboard
1. Information about a customer
1. An address
1. The names of the first 150 pokemon, in order
1. All the meals you serve in your restaurant
1. Details about a meal served by your restaurant, such as name, price, and allergy info
1. Details about all the meals your restaurant serves

---

## Compound Collections

Ruby lets you put any value inside an array or hash

So why not another array or hash?

---

## Menu

One variable `menu` containing an array

The array has 3 values, each is a hash

Each hash has two keys, `name` and `price`

Questions:

- What would the literal look like?

- How would you access data?

---

## Literal Syntax

```ruby zoom-12
menu = [
  {
    "name" => "beet salad",
    "price" => 6.75,
  },
  {
    "name" => "quiche",
    "price" => 10.00,
  },
  {
    "name" => "molten chocolate cake",
    "price" => 8.50,
  }
]
```

---

## Accessing Data

```ruby zoom-12
# The first element in the menu array is a hash
puts menu[0]
# => { "name" => "beet salad", "price" => 6.75 }

# Since "menu[0]" is a hash, we can apply more square brackets to it
puts menu[0]["name"]
# => beet salad

# We can also assign it to a variable
salad = menu[0]
puts salad["name"]
# => beet salad
```

We sometimes call this **drilling down** into the data structure

---

## Iteration

Write code to loop through the `menu` array and print out the name and price of each item

```ruby zoom-12 fragment
menu.each do |meal|
  puts "#{meal["name"]} --- $#{meal["price"]}"
end
```

---

## Layers

It can be helpful to think of each **layer** of a data structure independently

- What type of collection is this layer?

- What do the values contained in this layer represent?

<p class="small">Another way to ask this question is, what would you name the iteration variable?</p>

---

## Band Attendance

Now let's build the full version of our band attendance program

We want to store monthly rehearsal attendance numbers for each band member

**Question:** What steps can we take to break down the problem?

---

## Breaking Down the Problem

- Identify layers

- Write a hard-coded version of the data structure

- Write code for dealing with the inner layer

- Wrap it in code for dealing with the outer layer

---

## Hard-coded

```ruby zoom-12
member_attendance = {
  "Ada" => [4, 3, 5],
  "Grace" => [2, 4, 2],
  "Katherine" => [3, 4, 3],
}
```

---

## Inner Layer

```ruby zoom-12
attendance_requirement = 10
member_attendance = {
  "Ada" => [4, 3, 5], # ...Katherine and Grace...
}

name = "Grace"
attendance = member_attendance[name]

total = 0
attendance.each do |month|
  total += month
end

if total < attendance_requirement
  # ...
end
```

---

## Outer Layer

```ruby zoom-12
attendance_requirement = 10
member_attendance = {
  "Ada" => [4, 3, 5], # ...Katherine and Grace...
}

member_attendance.each do |name, attendance|
  total = 0
  attendance.each do |month|
    total += month
  end

  if total < attendance_requirement
    # ...
  end
end
```

---

## Stretch Goals

For if we have extra time

- Best attendance: report who had the best attendance overall

- User input: fill in the contents of the data structure with user data

- Dynamic attendance requirement: track the max attendance for each month, sum those for the total number of rehearsals, and take 2/3 of that as the attendance requirement

---

## Vocab

---

## Review Questions
