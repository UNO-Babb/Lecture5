# Lecture 5 - CYBR 2980
## Objectives
- Discuss & demonstrate string manipulations:
  - subscript operator
  - indexing
  - slicing a string
- Converting strings to numbers
- Converting numbers to strings

### Strings

### Indexing

### Slicing

### Looping in Strings

```
def isPalendrome(word):
  # check that the first letter is the same as the last
  # continue checking 2nd letter to 2nd from end, etc.

  return False


def main():
  word = input("Enter a word: ")

  if isPalendrome(word):

```

### String Methods

| Function |	Meaning |
| --- | --- |
| str.**capitalize(s)** | Copy of s with only the first character capitalized |
| str.capwords(s) | Copy of s; first character of each word capitalized |
| str.center(width) | Center s in a field of given width |
| count(sub) |
| find(sub) |
| join(list) |
| ljust(s, width) |
| lower(s) |
| lstrip(s) |
| repalce(s, oldsub, newsub) |
| rfind(s, sub) |
| rjust(s, width) |
| rstrip(s) |
| split(s) |
| upper(s) |


Count the number of occurrences of sub in s
Find the first position where sub occurs in s
Concatenate list of strings into one large string
Like center, but s is left-justified
Copy of s in all lowercase characters
Copy of s with leading whitespace removed
Replace occurrences of oldsub in s with newsub
Like find, but returns the rightmost postion
Like center, but s is right-justified
Copy of s with trailing whitespace removed
Split s into a list of substrings
Copy of s; all characters converted to uppercase
