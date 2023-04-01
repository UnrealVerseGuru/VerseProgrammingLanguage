### Proposed file structure

 * module A ```<public>```
   * module B ```<public>```
   * module C ```<internal> #by default```

----------------

module A ```<public>```

1. logs
2. tags
3. messages (non-local by API)
4. interfaces
5. constructors
6. class/struct definition
  * ``` <public>```
    * fields
      * editable 
    * events
    * methods
      * for Devices: OnBegin should be high 
    * ui
    * debug/temps
  * ```<protected>```
  * ```<private>```
7.  extension methods 

------------

### Naming Conventions
Although not forced by compiler naming convention helps with code readability.

 * **types**: lower_snake_case
  ```diff
  fort_character
  my_new_device
  ```
 * **variables** CamelCase
 * optionals: preferably statring with Opt, or Maybe..
```diff
MyabePlayer : ?player = false
DamageAmountOpt : ?int = false
```
 * `logic` variables with "b" prefix
```diff
bContainsWeapons<native><public>:logic = external {}
```

#### Functions naming
 * Getters start with "Get"
 ```diff
(InAgent:agent).GetFortCharacter<native><public>()<transacts><decides>:fort_character
```
 * Setters start with "Set"
 ```diff
SetText<native><public>(InText:message):void
```
 * returning `logic` might be distniguished with "Is" prefix
 ```diff
IsEnabled<native><public>():logic
```

### Comments
 * Preffer **multi-line block comment** for multi lined comments or **indentend comment**
```diff
<# This comment spans multiple lines, 
to avoid typing hashes all over the place preffer multi-line block comments #>

<#> Or use this indentend comment
    use 4 spaces to add it's contents
ThisFunctionIsNotCommentedOut()
```
 * 

### language reserved keywords
TODO
