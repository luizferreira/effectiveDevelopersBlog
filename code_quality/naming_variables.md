Names are everywhere in our code and having the ability to name variables, functions, classes, and packages well is essential to write readable and maintainable code. Here are some tips:

## Intention-Revealing Names ##

Names should reveal intent. So, `elapsed_time_in_seconds = 20` is better than `s = 20`.

## Avoid False Clues ##

Do not refer to a grouping of accounts as an `accountList` unless it's actually a `list`.

## Use Searchable Names ##

Single-letter names and numeric constants are hard to locate across a large body of text. It's easier to understand and find all occurrences of `MAX_DAYS_PER_MONTH` than the number `31`. You should use single-letter names only as local variables within a very limited scope.

## Class Names ##

Classes and objects should have nou or noun phrase names like Customer, Wikipage, Account, and AddressParser. Avoid words like Processor, Data, or Info in the name of a class. A class name should not be a verb.

## Method Names ##

Some people advocate that method names should always be verbs, like `post_payment`, `delete_page`, or `save`. My personal preference is to name functions and methods according to their side-effects:
* Those without side-effects shoud be named as nouns.
* Those with side-effects shoud read as verbs.

Example:

```
students.sort()  # side effect (change the state of the list); ideally, shouldn't return anything
sorted(students)  # no side effect (the original list is not affected); ideally, should always return a value
```

This is also related to the command-query separation principle. Commands (produce side effects) should be named as verbs and Queries (return something) should be named as nouns. The command-query separation principle states that if a routine have side effects (command), it shouldn't return a value; and if a routine returns something (query), it shouldn't have side effects.

## Pick one word per concept ##

Pick one word for one abstract concept and stick with it. For instance, it's confusing to have `fetch`, `retrieve`, and `get` as equivalent methods of different classes.


