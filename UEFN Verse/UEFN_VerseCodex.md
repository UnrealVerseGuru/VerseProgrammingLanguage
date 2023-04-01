# UEFN / Verse Codex
Attempt at standarization for style and structure of UEFN & Verse projects, feedback/your ideas more than welcome ! ❤️ search for **Verse Codex** on Fortnite forums

## Verse style guide

### Proposed file structure

 * module A ```<public>```
   * module B ```<public>```
   * module C ```<internal> #by default```

----------------

module A ```<public>```

1. logs
2. tags
3. messages <sub>(non-local by API)</sub>
4. interfaces
5. constructors
6. class/struct definition
  * ``` <public>```
    * events
    * fields
      * `@editable` should be high
    * methods
      * for Devices: `OnBegin()` should be high 
    * ui
    * debug/temps <sub>(good practive to keep it in one place)</sub>
  * ```<protected>```
  * ```<private>```
7.  extension methods 

------------

### Naming Conventions
Although not forced by compiler naming convention helps with code readability. Esp given limited capabilities of LSP atm

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
 * `<decides>` effect unless a getter might be distinguished with forming an question, e.g. "Try" or "Is" prefix
 ```diff
TrySelectNext<decides><transacts>():void
(V:vector3).IsFinite<public>()<computes><decides>:vector3
```
 * Setters prefix with "Set"
 ```diff
SetText(InText:message):void
```
 * `<suspends>` distinguished with "Async", pre/post
 ```diff
AsyncMoveTo()<suspends>:void
```
 * `<constructor>` with "Make"
 ```diff
MakeCountdownTimer<constructor><public>() := countdown_timer:
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

### language reserved keywords
_TODO_

## UEFN
### Asset naming conventions
For most stock UE assets working in UEFN follow [ue-5-style-guide](https://github.com/Allar/ue5-style-guide/commits?author=Allar)
