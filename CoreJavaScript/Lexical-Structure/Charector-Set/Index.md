# Basics of Charset

-JavaScript programs are written using the Unicode character set. Unicode is a superset of ASCII and Latin-1 and supports virtually every written language currently used

# Case Sensitivity
JavaScript is a case-sensitive language. This means that language keywords, variables,function names, and other identifiers must always be typed with a consistent capitalization of letters.\
Eaxmple :\
The while keyword must be typed “while,” not “While” or “WHILE.”

# Whitespace, Line Breaks, and Format Control Characters
*JavaScript ignores spaces that appear between tokens in programs.
*JavaScript also ignores line breaks
*Unicode format control characters (category Cf), such as RIGHT-TO-LEFT MARK(\u200F) and LEFT-TO-RIGHT MARK (\u200E), control the visual presentation of the text they occur in.

# Unicode Escape Sequences
 *Unicode escapes may appear in JavaScript string literals, regular expression literals, and in identifiers

 The Unicode escape for the character é:
 "café" === "caf\u00e9" // => true
 
 # Normalization
 *Unicode allows more than one way of encoding the same character. The string “é”, for example, can be encoded as the single Unicode character \u00E9 or as a regular ASCII e followed by the acute accent combining mark \u0301.