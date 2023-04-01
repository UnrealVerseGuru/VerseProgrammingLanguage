# UEFN / Verse Codex
Attempt at standarization for style and structure of UEFN & Verse projects, feedback/your ideas more than welcome ! ❤️ 
post your thoughts on [Fortnite forums](https://forums.unrealengine.com/t/verse-codex-naming-conventions-program-structure-code-clarity/838073)

Codex assumes strict access modifiers hygiene: expose only as much public/protected interface as needed.

## Verse style guide

### Proposed file structure

 * module A ```<public>```
   * module B ```<public>```
   * module C ```<internal> #by default```
 * module D ```<protected>```
 * module E ```<private>```
----------------

General rule: statics > events > functions > fields > else

module A ```<public>```

1. **module statics** like: logs, tags, constants, messages
2. **interfaces**
3. **constructors** <sub>(non-local by API)</sub>
4. **class/struct** definition
  * ``` <public>```
    * **statics** like: logs, tags, constants
    * **events**
    * **methods**
      * for Devices: `OnBegin()` should be high 
    * **fields**
      * `@editable` should be highest
      * messages <sub>(non-local by API)</sub>
    * **ui**
    * **debug/temps** <sub>(good practive to keep it in one place)</sub>
  * ```<protected>```
  * ```<private>```
5.  **extension methods** <sub>adhering to class from 4.</sub>

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

-------------

#### Functions naming
 * Getters start with "Get"
 ```diff
(InAgent:agent).GetFortCharacter<native><public>()<transacts><decides>:fort_character
```
 * `<decides>` effect might be distinguished with forming an question, e.g. "Try" or "Is" prefix
 ```diff
TrySelectNext<decides><transacts>():void
(V:vector3).IsFinite<public>()<computes><decides>:vector3
#note: for failable getters to distinguish them from non failable ones
TryGetCharacter()<decides><transacts>():character
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

-----------

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

--------------

## UEFN style guide
### Asset naming conventions
For most stock UE assets working in UEFN follow [ue-5-style-guide](https://github.com/Allar/ue5-style-guide/commits?author=Allar)
