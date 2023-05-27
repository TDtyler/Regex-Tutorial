# RegEx Hex Value Tutorial

## Introduction

RegEx, which is known for regualar expression. It is a sequence characters that defines a search pattern for text. When included in code or search algorithms, regular expressions can be used to find certain patterns of characters within a string, or to find and replace a character or sequence of characters within a string. They are also frequently used to validate input.

## Summary

In this tutorial we will be evaluating the the following regular expressions used to match HEX values:
`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

This RegEx consists of several componets such as, anchors, quantifiers, OR Operator, grouping and capturing and bracket expressions used in this regular expression.

## Table of Contents

- [RegEx Hex Value Tutorial](#regex-hex-value-tutorialRegEx-Hex-Value-Tutorial)
    - [Introduction](#introduction)
    - [Summary](#summary)
    - [Table of Contents](#table-of-contents)
    - [RegEx Componets](#regex-componets)
        - [Anchors](#anchors)
        - [Quantifiers](#quantifiers)
        - [OR Operator](#or-operator)
        - [Character Classes](#character-classes)
        - [Grouping and Capturing](#grouping-and-capturing)
        - [Bracket Expressions](#bracket-expressions)
    - [**Author**](#author)

    ## RegEx Componets

    ### **Anchors**

    Anchors alone do not match any regular expression. They assert something about the string (e.g. beginning, end) based on expressions/matching pattern next to the anchor.
    The ^ is an anchor that indicates that the beginning of the string must match the character #. # is used to distinguish a hexadecimal number from a decimal number. 

    ### **Quantifiers**

    Quantifiers are special characters that specify how many times a character or group of characters can be repeated.
    Example: 3{4} indicates that 3 must be repeated 4 times. matching string will be 3333.
    In our regex, {6} indicates that there are 6 instances of the string in the preceding bracket expression. That implies that this quantifier will allow exactly 6 characters in the string containing characters between a-f and/or integer between 0-9. {3} indicates that there are 3 instances of the string in the preceding bracket expression. That implies that this quantifier will allow exactly 3 characters in the string containing characters between a-f and/or integer between 0-9.

    ### **OR Operator**

    OR Operator: |

    Example: 2/7 indicates that either 2 or 7 or both integers are allowed in the string. 272, 222, and 777 are all matching patterns.

    In our case, that implies match with 3 character string containing lower case a-f and/or integer 0-9 OR a string with 6 characters containing lowercase a-f and/or integer between 0-9. A matching string has to have 3 or 6 character with the specified pattern. Anything other than 3 or 6 characters will not match.

    ### **Character Classes**

    A character class is a special notation that matches any one of a specified set of characters.

    Example: [0-9] This character class matches a single digit between 0 and 9

    In this case, the character class consists of lower case a-f and/or integer 0-9.

    ### **Grouping and Capturing**

    Description: The () groups the regular expression between them. The grouping treats multiple characters as a single unit. This can proof useful when extracting information using any programming language. This group of data will be exposed in the form of an array. Values can be accessed using an index on the result of the match.

    Example: (cat){4} 'catcatcatcat'. The unit character of 'cat' would need to repeat 4 times in the quantifier.

    ### **Bracket Expressions**

    Bracket expressions are special characters that specify a set or a range of characters to match.

    Example: [a-d 1-3] indicates that the string must include atleast 1 character that is between a and d or 1-3

    In our reg ex, the bracket [] expression indicates matching a string that has any lower case character between a-f or any integer between 0-9

    ## **Author**

    This tutorial was made by TDtyler. I'm currently a student in the Georgia Tech full stack developer coding bootcamp.











