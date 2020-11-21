# Algorithms - Objectives
## Define an algorithm and relate it to problem solving.
### Informal Definition
An Algorithm is a Step-By-Step method for solving a problem.
Wording should be consistent & Generalized
### Formal Definition
An **Ordered Set** of **unambigous steps** that **produces a result** and **terminates in a finite time**

## Define three construct and describe their use in algorithms.
### Sequence
A Sequence of Actions
```
action 1
action 2
action 3
```
### Decision
Conditional Actions, Also includes Selection?
```
if condition
	action 1
else 
	action 2
```
### Repetition
Looping over actions
```
for elements in n
	action
```


## Describe UML diagrams and pseudocode and how they are used in algorithms.
Gives an overview of what the Algorithm does, without any technical details or specific syntax

## List basic algorithms and their applications.
- Summation of a List
- Product of a List
- Finding Smallest & Largest Numbers of a List
- Sorting
- Searching
## Describe the concept of sorting and understand the mechanisms behind three primitive sorting algorithms.
These basic sorting algorithms all have something in common.

Two Sublists, sorted and unsorted, seperated by an `imaginary wall`

[Watch a visualization on how the sorting works](https://www.youtube.com/watch?v=kPRA0W1kECg), it is hard to explain via text or images

### Selection Sort
`Select` the smallest element in the unsorted sublist, and swap it with the element one index ahead in the end of the sorted sublist.

### Bubble Sort
This algorithm has a `bubbling` effect, as the larger elements graudally move upwards, which is why it is called a `bubble sort`

### Insertion Sort
Select the smallest element in the unsorted sublist, but `insert` it into the sorted sublist. 

Selection -> Swap
Insertion -> Insert

## Describe the concept of searching and understand the mechanisms behind two common searching algorithms.
### Sequential/Linear Search 
Search from the beginning to the end, element by element

Slow for large amount of elements

### Binary Search
List must be sorted to use this algorithm!

Splits search space in half every iteration, until the

Very efficient with many elements

## Define subalgorithms and their relations to algorithms.
Algorithms and Subalgorithms can be split into smaller chunks called `subalgorithms`

Subalgorithms can also be broken down into smaller `subalgorithms`

## Distinguish between iterative and recursive algorithms
Iteration -> Loops
Recursion -> Algorithm calling itself

[Back to Main Page](../README.md)
