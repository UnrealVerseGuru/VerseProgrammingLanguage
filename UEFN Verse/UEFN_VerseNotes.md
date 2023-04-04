DISCLAIMER: This is very much old & WIP, I've dumped few thoughts from UEFN release skimming over docs, will soon fix this and fill with info.

### UEFN Verse general info:
- case sensitive globally. no strict naming conventions, You can do whatever you like, but recommendation: CamelCase values, lower_case types (snake_case for long types)
- no semicolons to finish statement
- indentation defines scoping
- member functions and classes are overrideable by default, `override` specifier required when overriding

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
# emojiis allowed
"I ❤️ Verse"
```
- `float`
```diff
10.5
```
- `int`
```diff
99
```
- `logic` usual boolean equivalent with either: false, true
```
false
var TargetLocked : logic = false
```
- `void` 

#### keywords
- `set`
```diff
# changes mutable variable value
set Coins = 22
```
- 

#### operators
 * query `?` postfix, use to check if `logic` is true or false
 ``` diff
 if (IsMorning?):
    Say("Good Morning!")
 ```
 * failable `=` infix, to test if two logic values are equal
 ```diff
 # Initialize logic variables for demonstration purposes.
var TargetLocked : logic = false
var WeaponEquipped : logic = true
	
# Determine whether or not the "unavailable action" icon is appropriate.
if (WeaponEquipped <> TargetLocked):
    # The icon should show up, because the player appears to be trying to
    # attack, but is missing either a weapon or a target.
    ShowUnavailableIcon()
```
 * `and`, `or` infix
``` dif
if (Tired? or SchoolTomorrow?):
    set WhatToWatch = "your eyelids"
else if (FriendsAvailable?):
    set WhatToWatch = "a movie with your friends"
else: 
    set WhatToWatch = "cartoons"
```

#### logging
```diff
CoinsAmount : int = 2
# string taking curly braces "{}" allows operation evaluation before Print() gets executed:
Print(" 2 + Coins amount = {2 + CoinsAmount}")
# Logs: 2 + Coins amount = 4

Print(" Concatenated string: {"I " + "❤️ " + " Verse"}")
# Logs: Concatenated string: I ❤️ Verse
```

#### conditional expressions
 - `if` `else`
 ```diff
var Tired: logic = false
var WhatToWatch: string = “nothing”

if (Tired?):
	set WhatToWatch = “your eyelids” #note indentation defines scope, if Tired? = true, only this expression will be evaluated, else: scope will be omitted
else:
	set WhatToWatch = “cartoons”

Print(“You should watch {WhatToWatch}”)

# logs: You should watch cartoons
```

#### functions
* function (routine) declaration
```diff
#function signature:
# name() : type =
    #codeblock/body has local scope
    
PrintHelloWorld() : void = 
    Print("Hello World")
```
 * function call
```diff
PrintHelloWorld()
```
 * member functions: **methods**
 ```dif
# call a member function 
Cat.Pounce()
 ```

 * Calling method that can fail/succeed, used with `<decides>` **specifier** **effect** in failure context
```diff
# explicit notation for querying failable function in failure context
if (FailableMethod[]):
	Print("Failable function succeeded")
```
 * `return` works mostly like cpp
```diff
WIP
```

### classes
 * **composite** type made of bundle of data from other **types**
 * inheritance by subclasses
 * methods - member functions

### attributes `@`
 * `@editable`
	* not supported for classes that aren’t `<concrete>`
```diff
# DefaultCreativePropAsset must be used for creative_prop_asset type, other types can instantiate normally with {} notation
@editable
PropAssetRef : creative_prop_asset = DefaultCreativePropAsset
```
