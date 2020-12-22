# Automation


## Regular Expressions in Python
Regular Expressions, often shortened as regex, are a sequence of characters used to check whether a pattern exists in a given text (string) or not.
In Python, regular expressions are supported by the re module. 
That means that if you want to start using them in your Python scripts, you have to import this module with the help of import:
```
import re
```

#### Basic Patterns: Ordinary Characters
You can easily tackle many basic patterns in Python using ordinary characters. 
Ordinary characters are the simplest regular expressions. 
They match themselves exactly and do not have a special meaning in their regular expression syntax.

Examples are `'A', 'a', 'X', '5'.`

Ordinary characters can be used to perform simple exact matches:

```
pattern = r"Cookie"
sequence = "Cookie"
if re.match(pattern, sequence):
    print("Match!")
else: print("Not a match!")
```

Match!
Most alphabets and characters will match themselves, as you saw in the example.

The `match()` function returns a match object if the text matches the pattern. 
Otherwise, it returns `None`. 

Do you notice the `r` at the start of the pattern Cookie?
This is called a raw string literal. 
It changes how the string literal is interpreted. Such literals are stored as they appear.

For example, `\` is just a `backslash` when prefixed with an r rather than being interpreted as an escape sequence.
Sometimes, the syntax involves `backslash-escaped` characters, and to prevent these characters from being interpreted as escape sequences; you use the raw `r` prefix.



#### Wild Card Characters: Special Characters
Special characters are characters that do not match themselves as seen but have a special meaning when used in a regular expression. 
For simple understanding, they can be thought of as reserved metacharacters that denote something else and not what they look like.


`.` - A period. Matches any single character except the newline character.

`^` - A caret. Matches the start of the string.

`$` - Matches the end of string.

`[abc]` - Matches a or b or c.

`[a-zA-Z0-9]` - Matches any letter from (a to z) or (A to Z) or (0 to 9).

`\` - Backslash.

`\w` - Lowercase 'w'. Matches any single letter, digit, or underscore.

`\W` - Uppercase 'W'. Matches any character not part of \w (lowercase w).

`\s` - Lowercase 's'. Matches a single whitespace character like: space, newline, tab, return.

`\S` - Uppercase 'S'. Matches any character not part of \s (lowercase s).

`\d` - Lowercase d. Matches decimal digit 0-9.

`\D` - Uppercase d. Matches any character that is not a decimal digit.

`\t` - Lowercase t. Matches tab.

`\n` - Lowercase n. Matches newline.

`\r` - Lowercase r. Matches return.

`\A` - Uppercase a. Matches only at the start of the string. Works across multiple lines as well.

`\Z` - Uppercase z. Matches only at the end of the string.

`\b` - Lowercase b. Matches only the beginning or end of the word.


### Repetitions

`+` - Checks if the preceding character appears one or more times starting from that position.

`*` - Checks if the preceding character appears zero or more times starting from that position.

`?` - Checks if the preceding character appears exactly zero or one time starting from that position.

`{x}` - Repeat exactly x number of times.

`{x,}` - Repeat at least x times or more.

`{x, y}` - Repeat at least x times but no more than y times.



## shutil — High-level File Operations

The shutil module includes high-level file operations such as copying and archiving.

#### Copying Files
`copyfile()` copies the contents of the source to the destination and raises IOError if it does not have permission to write to the destination file.

```
shutil_copyfile.py
import glob
import shutil

print('BEFORE:', glob.glob('shutil_copyfile.*'))

shutil.copyfile('shutil_copyfile.py', 'shutil_copyfile.py.copy')

print('AFTER:', glob.glob('shutil_copyfile.*'))
```

Because the function opens the input file for reading, regardless of its type, special files (such as Unix device nodes) cannot be copied as new special files with copyfile().

```
$ python3 shutil_copyfile.py

BEFORE: ['shutil_copyfile.py']
AFTER: ['shutil_copyfile.py', 'shutil_copyfile.py.copy']
```

The implementation of `copyfile()` uses the lower-level function `copyfileobj()`. While the arguments to `copyfile()` are filenames, the arguments to `copyfileobj()` are open file handles. The optional third argument is a buffer length to use for reading in blocks.

