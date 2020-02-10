# Lecture 5 - CYBR 2980
## Objectives
- Discuss & demonstrate string manipulations:
  - subscript operator
  - indexing
  - slicing a string
- Converting strings to numbers
- Converting numbers to strings

### Strings
In Python, Strings are lists of bytes representing Unicode characters. However, Python does not have a character data type, a single character is simply a string with a length of 1.
```
>>> print("Hello")
>>> word = "Hello"
>>> print(word)
```
### Indexing
Square brackets can be used to access elements of the string. Since a string is a list of individual letters, we can look at a spot in the list using the index position in a square bracket. This list is zero-indexed, meaning that the first spot is str[0].
```
>>> word = "hello"
>>> print(word[1])
>>> print("hello"[1])
```
### Slicing
Beyond looking at a single letter of a string, we can look at a selected range of the string. This range denoted by a square bracket with the starting index (inclusive) and the ending index (exclusive).
```
>>> word = "strawberry"
>>> print(word[2:5])
```
### Looping in Strings
Since a string is a list of characters, we can iterate across this list. One method is to use the index positions from zero to the length of the string.  
```
>>> word = "Hello"
>>> index = 0
>>> while(index < len(word)):
...   print(word[index])
```
In python, the for-loop iterates across a list, we can use the string as a list.
```
>>> sentence = "This is a test"
>>> for ch in sentence:
...   print(ch)
```
We can use the index position to test elements of the word... in this case we are trying to determine if a word is a palindrome. A palindrome is a word (or phrase) that is the same forward and backward.
```
def isPalindrome(word):
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
| str.**capitalize()** | Copy of str with only the first character capitalized |
| str.**capwords()** | Copy of str; first character of each word capitalized |
| str.**center(width)** | Center str in a field of given width |
| str.**count(sub)** | Count the number of occurrences of sub in str |
| str.**find(sub)** | Find the first position where sub occurs in str |
| str.**join(list)** | Concatenate list of strings into one large string |
| str.**ljust(width)** |Like center, but str is left-justified |
| str.**lower()** | Copy of str in all lowercase characters |
| str.**lstrip()** | Copy of str with leading whitespace removed |
| str.**repalce(oldsub, newsub)** | Replace occurrences of oldsub in str with newsub |
| str.**rfind(sub)** | Like find, but returns the rightmost position |
| str.**rjust(width)** | Like center, but str is right-justified |
| str.**rstrip()** | Copy of str with trailing whitespace removed |
| str.**split()** | Split str into a list of substrings |
| str.**upper()** | Copy of str - all characters converted to uppercase |


### Formatted Print
Formatted print statements are often useful, especially when you want to have a mix of numbers with decimals that need to be inserted in a larger string.

```
>>> name = "Jen"
>>> temp = 22
>>> print("Hello %s. The temperature today is %d degrees." %(name, temp))
```
#### Placeholder types
| Symbol | Type |
| --- | --- |
| %s | string |
| %d | integer |
| %f | float |
| %x | hexadecimal |
| %c | character |

With numeric values, padding can be used to ensure that the values have uniform size.
```
>>> for i in range(10):
...     num = random.random() * 100
...     print("%2.2f" %(num))
```

### Converting types
In programming languages, numbers and words are different datatypes. The number 5 is not the same as the string "5". To use math, we need to make sure that the values are numeric. To print, we need to make sure that values are strings.
```
>>> age_str = input("Enter your age: ")
>>> age_int = int(age_str)
>>> age_in_five = age_int + 5
>>> print("In five years you will be " + str(age_in_five))
```
### Quiz
1. What is the output of the following statement?  
  str = "Omaha"  
  print(str[1:3])
  - Oma
  - mah
  - ma
  - aha

1. What is the output of the following statement?  
  sentence = "Hello world"
  print(len(sentence))

1. What is the value of str after the following statements?
  str = "hello"
  str = str.capitalize()
  str.upper()
  print(str)
  - Hello
  - hello
  - HELLO

1. Which of the following will print a number with 3 decimal point precision?
  - print("%3.2f" %(num))
  - print("%2.2d" %(num))
  - print("%3.5s" %(num))
  - print("%2.3f" %(num))

1. UNO IDs are determined by a first initial, middle initial, and last name. Given the following, how would you create a username?   
first = input("Enter first name: ")  
middle = input("Enter middle name: ")  
last = input("Enter last name: ")  
