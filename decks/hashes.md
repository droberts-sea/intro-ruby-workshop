@snap[midpoint span-100]
# Hashes
@snapend

---

# TODO Agenda

---

## Learning Goals


---

## Motivation

Data isn't always organized by number

Sometimes we want to be able to **access data by name**

<li>**Look up** the address of a business</li>

<li>**Store several properties related to one object**, like the sender, recipients, subject and text of an email</li>

<li>Track number of rehearsals attended for each member of a band</li>

---

## Hashes

@snap[west span-50]
Hashes are used to store a set of **associations** between keys and values

The hash gets a **name**

We use **keys** (strings) to refer to individual values

Hashes are sometimes called **dictionaries**
@snapend

@snap[east span-50]
![](assets/images/dictionary.jpg)
@snapend

---

## Hash Syntax

```ruby zoom-12
# Hash literals use curly braces { and }
# keys and values are associated using a "hash rocket" =>
# key-value pairs are separated by commas
email = {
  "sender" => "katherine@adadev.org",
  "recipient" => "ada@adadev.org",
  "subject" => "Orbital trajectories"
}

# Using a hash looks a lot like using an array
# Access values using the associated key
puts email["subject"]

# Add a new key-vaue pair
email["text"] = "Hi Ada..."
```
---

## A Word on Symbols

There is another syntax for hashes that uses a different data type called a **symbol** as its keys

You may have seen this if you've studied Ruby independently (lots of :colons)

For simplicity and time, **today we will limit ourselves to string keys**

Be aware as you study that string keys and symbol keys aren't totally compatible

---

## Hashes Exploration

Keeping in mind your experience with arrays, take some time to explore hashes. Can you...

<ul class="small">
<li>Use a variable as the key or value in a **hash literal**?</li>

<li>Use a variable as the key to lookup or set a value?</li>

<li>Use the same key twice?</li>

<li>Use the same value twice?</li>

<li>Print a hash to the screen with `puts`?</li>

<li>Look up the value for a key that isn't in the hash?</li>

<li>Use data types other than strings as keys and values?</li>
</ul>

How are arrays and hashes similar? How are they different?

---

## Hash Iteration

```ruby zoom-12
email = {
  "sender" => "katherine@adadev.org",
  "recipient" => "ada@adadev.org",
  "subject" => "Orbital trajectories"
}

puts "Email details:"
email.each do |key, value|
  puts "#{key}: #{value}"
end
```

Hashes store a set of key-value pairs, so when you iterate you get two variables

---

## Band Attendance

Set the current band attendance program aside for now 
<p class="small">We'll come back to it</p>
<br>
Write a program that...

<ul class="small">
<li>Asks the user for a number of members</li>
<li>Collects a name and total rehearsal attendance for each member</li>
<li>Prints a message to the screen for each member indicating whether they have been to at least 10 rehearsals</li>
</ul>

You may want to reuse parts of your old program

---

## Scaling Up

**Collections** like arrays and hashes, along with **iteration**, are key for more complex programs

They allow our programs to **handle more data without more code**

We call this idea **scaling up**

---

## Vocab

---

## Review Questions