### UEFN Verse general info:
- _case sensitive_
- no semicolons to finish statement

**Comments**
```diff
# This is single-line comment

SomeVar : int = 3 #here comment starts, single-line comments extends till end of line

1<# inline block comment, can be put inbetween expressions and dont change them #>+2


# multi-line block comment
DoThis()
<# And they
can run multiple
long lines #>
DoThat()

<# nested block comment <# like this #> #>

# indented comment: everyting indented four spaces over after <#> is part of the code comment, anything not having four spaces is not:

<#>
    Here is a long
    description spanning
    multiple lines.
DoThis() # This expression is not part of the indented comment
```
 
#### Variables
- **Constant variables declaration**
```diff
# name : type = value
WeekDaysNum : int = 7
# initialization is required at declaration
# note spaces do not matter
WeekDaysNum:int=7 

```
#### **Mutable variables declaration**
- differ from constants only by ```var``` keyword
```diff
# var name : type = value
var Coins : int
# note no initialization required
```

#### basic types

 - `string`
```diff
"This is string"
```
- `float`
```diff
10.5
```
- `int`
```diff
99
```
- `logic` usual boolean with either: false, true
```
false 
```
#### keywords
- `set`
```diff
# changes mutable variable value
set Coins = 22
```
- 

#### logging
```diff
CoinsAmount : int = 2
# string taking curly braces "{}" allows operation evaluation before Print() gets executed:
Print(" 2 + Coins amount = {2 + CoinsAmount}")
# Logs: 2 + Coins amount = 4

# emojiis allowed
Print(" Concatenated string: {"I " + "❤️ " + " Verse"}")
# Logs: Concatenated string: I ❤️ Verse
```
