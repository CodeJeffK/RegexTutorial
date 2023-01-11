# Regex Tutorial

The purpose of this gist is to explain what a regular expression is and how to use them. Regular expressions (Regex) can be used 
when one is trying to match a certain character combination within a string. In short, a regex or regular expression, is a series 
of characters and symbols used to match strings against a desired format or content.

## Summary

In this tutorial, I will be describing and explaining a regex to match emails. The following code can be used for matching emails. 
One use for this regex code is validation to make sure an email input matches the correct format.

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

A regex is always contained by forward slashes '/' so that the computer knows where to start reading the regex and where it ends. 
Other components include: '.' which will match any single character, '' which is an escaping character, it is used to escape the regex 
and instruct the computer to interpret the following character literally, '$' matches any string where the preceeding text is present at 
the end of a string, '^' matches any string where the following text is present at the beginning of a string, '[]' matches any single character in a range or set within the brackets, '|' indicates an 'or' operator within the regex, lastly '()' is used to group expressions.

### Anchors

Anchors are symbols used to match strings at either the beginning or end of the string. Examples of anchors include the carat and dollar sign. As described earlier, the carat matches a string starting from the beginning. In the matching email code, 

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`, 

the anchors are the `^` and the `$`. This code specifically is saying that we are looking for something that starts with a specific string

`^([a-z0-9_\.-]+)` 

and also has to end with a specific string.

`.([a-z\.]{2,6})$`.

So, it must start and end with the given parameters within the code. If it does not, then it is not a match. 

### Quantifiers

A quantifier is used to determine how many times a specific character or group of characters needs to be present in order to have a match. For instance, if we used the following code in our regex, `xyz+` then this will match any string xy followed by at least one z. So, if we look at our code for matching the email:

`([a-z0-9_\.-]+)` 

this will match any string that contains a-z, 0-9, _, ., or -. The quantifier `+` means that it has to contain at least one of these 
parameters in order to match the regex.

### OR Operator

The OR operator is denoted with a single '|'. This logic operator is the same as the OR operator used in JavaScript which is denoted by '||'. This allows for matching against multiple options in the regex. A simple example would be matching '/flower|bush/' against the string 'The flower on the tree is nice'. The regex would match flower since it may match either flower OR bush in the evaluation. It would also return true against the string 'The bush is large'. However it would return false when evaluated against the string 'Deciduous trees lose their leaves each autumn' as neither the values of flower or bush are present in the string. This allows for evaluating expressions for multiple substrings where the desired terms are not always the same.

### Character Classes

Character classes allow you to match a symbol from a set of characters. `\d` is present in the given matching email code and what it will match a single letter character, a-z, after the `@` sign in the email address. Basically ensuring that a letter is matched after the `@` in the email and not a number or special character.  

### Flags

Flags are placed at the end of a regex out side of the closing '/'. These flags allow for things like gloabal searching, case insensitive searching or allowing anchors to match newline characters allowing for multiline searches. The flags are:

* g which stands for "global" which will allow for matching all the instances within a string that follow the matching guidelines set in the regular expression.
* m which stands for "multiline" which will search line by line rather than searching through a string as a whole. 
* i which stands for "insensitive" will make the 
regular expression case-insensitive, so capitals and lower-case letters will not deture the matching.

### Grouping and Capturing



### Bracket Expressions



### Greedy and Lazy Match



### Boundaries



### Back-references



### Look-ahead and Look-behind



## Author


A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
