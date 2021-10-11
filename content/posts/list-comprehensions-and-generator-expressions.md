---
title: "List Comprehensions and Generator Expressions"
date: 2021-10-11T15:48:57+01:00
draft: false
---
*Book:* Fluent Python
*Author:* Luciano Ramalho
*Excerpt:* Chapter 2, List Comprehensions and Generator Expressions

List comprehensions are a more readable way to make a `list` than appending elements to a list with `for` loops. This is because `for` loops can be used for many different tasks but list comprehensions are only used for one thing - building lists. Their intent is explicit.

## List Comprehension Syntax
`[list_element for thing in things]`    

You can initialise other types of sequence with generator expressions

## Generator Expressions
The syntax is the same a list comprehensions but with normal parentheses instead of square brackets. 

For example for a Tuple:

`tuple(list_element for thing in things)`   

Using a generator expression to make tuples over a list comprehension and `for` loop saves memory because it yields items one by one using the iterator protocol instead of making a whole list to store in memory to be iterated over.
