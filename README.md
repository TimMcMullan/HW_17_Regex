# HW_17_Regex

# Regular Expression to validate an American Express Credit Card input- `^3[47][0–9]{13}$`

The popularity, and ultimately, the relevance and usefulness, of the Internet, specifically, the World Wide Web, was gretly impacted when we learned how to buy and sell things online.  Credit card validation was a crucial part of this.  Processing the transaction is one thing, and this expression does not go that far, but it did allow programmers to validate the data was input correctly (not typographical errors) and could represent an actual card.  We will look at how the American Express card can be validated.

## Summary

The American Express card is seen as a high end credit card.  However, it has the simplest validation process of the major credit cards (VISA, MasterCard, and Discover).  We will break down the regular expression one could use in a function to verify the parameters of the card.  Specifically, the regular expression ^3[47][0–9]{13}$ will tell us that the card has the right number of digits, and verify certain digits are the correct value to qualify as an American Express Card.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors
Anchors used in our validation are `^` and `$`.  `^` is used to designate that a string (set of values) starts with the letter, or sequence, directly following `^`.  `$` works the same for the end of the string.
For our validation, which starts with `^3`, we are declaring the first value must be the number 3.  The examined item also must end with at least 13 numbers whose values could each be any single number.  This is designated by `{13}$`.

### Quantifiers
Quantifiers are deployed right next to the symbol they influence. Multipliers include `_*, +, ?, and {}`, and may be used in  tandom.  Our expression only uses the `{}` quatifier.  The `{}` enclose the number 13, representing there must be 13 digits that meet the criteria of the element next to it, which in our case is `[0-9]`, which is explained below.  For the purpose of explaining our quantifier, we'll simply state the part of the expression `[0-9]{13}` means we must see 13 instances of number.


### Bracket Expressions
Bracket Expressions contain symbols to be found.  How the symbols are shown in the bracket impacts the search.  For example, if multiple letters are shown in the brackets next to each other, any of the letters shown meet the search criteria.  `[abc]` means that a string with a, b, or c in it satisfies the search.  The expression `[a-c]` is exactly the same, and is usually used in larger sets of acceptable characters.  For our search, the bracket expression `[0-9]` represents that the character must be a digit.  This expression is extended to require 13 of these characgers, as we explained in the Quantifiers section.

### The OR Operator
You may have put together that our bracket expression is also an "or" operator.  This is why `[0-9]` represents any number.  Another symbol, `|`, can act similarly, but is not used in our expression.

## Author

Tim Mcmullan is an aspiring full-stack web-developer with a trendy interest in Regular Expressions and American Express cards.  Find out more about him by visiting his github profile below.

[Tim's github link][github_link]

[github_link]: https://www.github.com/TimMcMullan