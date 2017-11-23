Names are everywhere in our code and having the ability to name variables, functions, classes, and packages well is essential to write readable and maintainable code. Here are some tips:

## Intention-Revealing Names ##

Names should reveal intent. So, `elapsed_time_in_seconds = 20` is better than `s = 20`.

## Avoid false clues ##

Do not refer to a grouping of accounts as an `accountList` unless it's actually a `list`.

## Use Searchable Names ##

Single-letter names and numeric constants are hard to locate across a large body of text. It's easier to understand and find all occurrences of `MAX_DAYS_PER_MONTH` than the number `31`. You should use single-letter names only as local variables within a very limited scope.

