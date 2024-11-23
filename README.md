# Learning Haskell Finally !

Trying to learn Haskell to understand Functional Programming properly and be 
able to solve haskell-99 and work with languages like Rust and Scala which 
borrow very heavily from functional paradigms of thinking.

## Table of Contents

* [Chapter 1 : Features and Syntax](#chapter-1-features-and-syntax)
* [Chapter 2 : Constructs](#chapter-2-constructs)
* [Chapter 3 : More Functions + Function Composition](#chapter-3-more-functions--function-composition)
* [Chapter 4 : Modules in Haskell](#chapter-4-modules-in-haskell)
* [Chapter 5 : I/O in Haskell](#chapter-5-i-o-in-haskell)
* [Chapter 6 : Functors in Haskell](#chapter-6-functors-in-haskell)
* [Chapter 7 : Monads in Haskell](#chapter-7-monads-in-haskell)
* [Chapter 8 : Monoids in Haskell](#chapter-8-monoids-in-haskell)
* [Chapter 9 : Zippers in Haskell](#chapter-9-zippers-in-haskell)

### Chapter 1 : Features and Syntax
In Haskell, we just tell Haskell to do things and not bother too much about the 
procedural implementation of things. This is a new way of thinking because of  
the fact that when we think funtionally, we acknowledge that there are only so 
many functions available to use and we need to use them creatively to arrive at 
results. 

This thinking paradigm allows developers to write less and more predictable code 
and not write a separate function for everything. It also encourages us to handle 
edge cases properly within the confines of our available functions. Think within 
the box to think outside the box.

**Lazy Evaluation:** Haskell uses something called lazy-evaluation to avoid 
the compute cost for things which are not being used. Suppose, you have an array 
of a million elements that you need to take the sum of. But if you are not going 
to use this sum anywhere then Haskell is not going to do the computation for you 
and instead just skip it. (This is similar to Go-compiler's behaviour about 
complaining with regards to unused variables).

```haskell
let infiniteList = [1..]
take 10 infiniteList
```

There, the execution engine evaluated the infiniteList only for 10 elements and 
not for anything more than that. This is lazy!

When the `evaluation engine` finds an expression that must be evaluated, then a 
`thunk` data-structure is created and this DS collects all the information that 
is required for that specific evaluation and a pointer to that DS.

> This is also related to Garbage collection which will be discussed later.

The first element in the array defines the datatype of the array
```haskell
>> [True, False, "string"]
>> ["string", True]
```

Both of these lines throw different errors where the first one expect the last 
element to be a Bool, the second one expects the last element to be a `[Char]`
(character array).

### Chapter 2 : Constructs
1. **Pattern Matching**

2. **Guards**

3. **Where Clause**

4. **Recursion**

5. **Higher Order Functions**

6. **Lambda Expression**

### Chapter 3 : More Functions + Function Composition
### Chapter 4 : Modules in Haskell
### Chapter 5 : I/O in Haskell
### Chapter 6 : Functors in Haskell
### Chapter 7 : Monads in Haskell
### Chapter 8 : Monoids in Haskell
### Chapter 9 : Zippers in Haskell
