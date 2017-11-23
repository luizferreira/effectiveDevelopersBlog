# Meaningful Names in Code #

Names are everywhere in our code and having the ability to name variables, functions, classes, and packages well is essential to write readable and maintainable code. Here are some tips to increase the readability of your code by creating meaningful names (mostly based on the book Clean Code by Robert Martin):

## Intention-Revealing Names ##

Names should reveal intent. So, `elapsed_time_in_seconds = 20` is better than `s = 20`.

## Avoid False Clues ##

Do not refer to a grouping of accounts as an `accountList` unless it's actually a `list`.

## Use Searchable Names ##

Single-letter names and numeric constants are hard to locate across a large body of text. It's easier to understand and find all occurrences of `MAX_DAYS_PER_MONTH` than the number `31`. You should use single-letter names only as local variables within a very limited scope.

## Class Names ##

Classes and objects should have noun or noun phrase names like Customer, Wikipage, Account, and AddressParser. Avoid words like Processor, Data, or Info in the name of a class. A class name should not be a verb.

## Method Names ##

Some people advocate that method names should always be verbs, like `post_payment`, `delete_page`, or `save`. My personal preference is to name functions and methods according to their side-effects:
* Those without side-effects should be named as nouns.
* Those with side-effects should be named as verbs.

Example:

```
# side effect (change the state of the list); ideally, shouldn't return anything
students.sort()

# no side effect (the original list is not affected); ideally, should always return a value
sorted(students)
```

This is also related to the command-query separation principle. Commands (produce side effects) should be named as verbs and Queries (return something) should be named as nouns. The command-query separation principle states that if a routine has side effects (command), it shouldn't return a value; and if a routine returns something (query), it shouldn't have side effects.

## Pick One Word Per Concept ##

Pick one word for one abstract concept and stick with it. For instance, it's confusing to have `fetch`, `retrieve`, and `get` as equivalent methods of different classes.

## Solution Domain Names ##

Remember that the people who read your code are also programmers. So go ahead and use computer science terms, algorithm names, pattern names, math terms, and so forth. What programmer would not know what a JobQueue was?

## Problem Domain names ##

When there is no "programmer-eese" for what you're doing, use the name from the problem domain. At least the programmer who maintains your code can ask a domain expert what it means.

Separating solution and problem domain concepts is part of the job of a good programmer and designer. The code that has more to do with problem domain concepts should have names drawn from the problem domain.

## Add Meaninful Context ##

Variables should have clear contexts. The variable `state`, for instance, can mean a lot of things. So, use `address_state` rather than only `state`.
