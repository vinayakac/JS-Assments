## Text

A string is an immutable ordered sequence of 16-bit values, each of which typically represents a Unicode character—strings are JavaScript’s type for representing text. The length of a string is the number of 16-bit values it contains.

JavaScript’s strings (and its arrays) use zero-based indexing: the first 16-bit value is at position 0, the second at position 1 and so on.

## 1.String Literals

To include a string literally in a JavaScript program, simply enclose the characters of the string within a matched pair of single or double quotes (' or ").

Example :

"" // The empty string: it has zero characters
'testing'
"3.14"
'name="myform"'
"Wouldn't you prefer O'Reilly's book?"
"This string\nhas two lines"
"π is the ratio of a circle's circumference to its diameter"

If you need to include a newline character in a string literal,use the character sequence \n (documented below):

"two\nlines" // A string representing 2 lines written on one line
"one\

## 2. Escape Sequences in String Literals

The backslash character **('\')** has a special purpose in JavaScript strings. Combined with the character that follows it, it represents a character that is not otherwise representable within the string. For example, \n is an escape sequence that represents a newline character.

![Alt text](/escape-sequence.png?raw=true "Title")

