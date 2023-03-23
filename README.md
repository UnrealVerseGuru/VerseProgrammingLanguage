# ❤ Verse programming language
**Functional logic language developed by Epic Games** - repo of all informations, official resources and snippets

Also called "MaxVerse" by [SPJ](https://simon.peytonjones.org/): "Analogy Haskell" "built on top of **VC**"

<details>

***<summary>🔴Official descriptions of language by its authors</summary>***

   ----------------------
### General descritpions
 * Verse is a functional logic language (like Curry or Mercury)
 * Verse is a declarative language: a variable names a single
 value, not a cell whose value changes over time
 * Verse is lenient but not strict:
  * Like strict: everything gets evaluated in the end
  * Like lazy: functions can be called before the argument has a value
 * Verse has an unusual static type system: types are firstclass values
 * Verse has an effect system, rather than using monads
 * ***Verse is open: Open spec, open-source compiler, verifier, published papers, runtime under permissive open-source license with no IP encumberances***
 * Mutable state, I/O, and other effects
 * Pervasive transactional memory
 * Structs, classes, inheritance
### Ideas & visions
 * Kick functional logic programming out the lab and into the mainstream
 * Learnable as a first language (c.f. Javascript yes, C++ no)
 * Stretches from end users to professional developers
 * Transactional memory at scale
 * Very strong stability guarantees
 * A radical new approach to types
 * Extensible: mechanisms for the language to grow over time, without breaking code
 
   ----------------------
</details>

<sub> do not confuse with: ~~https://github.com/verse-lang/verse https://github.com/Idyllei/verse-pl </sub>~~

#### Official materials:
  * ▶[Beyond Functional Programming: The Verse Programming Language (Simon Peyton Jones)](https://www.youtube.com/watch?v=832JF1o7Ck8&ab_channel=SkillsMatter) <sub>Dec 2022 SPJ</sub>
    * 📟 [^slide deck](https://simon.peytonjones.org/assets/pdfs/haskell-exchange-22.pdf)
   * ▶ **[The Verse programming language GDC 2023](https://youtu.be/teTroOAGZjM?t=22494)**
-------------
# 💙 Verse in [UEFN - Unreal Editor For Fortnite](https://store.epicgames.com/en-US/p/fortnite--uefn)
**Called "ShipVerse" by SPJ or "BetaVerse"(Tim Sweeney) "very conservative subset" of Verse programming language avilable in UEFN, sometimes related as "Verse scripting"**



UEFN Verse does differ a bit from Verse programming language and what we see in VC

[I've made video summarizing how Verse might play in UEFN and to clarify these 3 different terms: CoreVerse, ShipVerse, MaxVerse](https://youtu.be/Xon9r3piIIw?t=251) <sub>at 4:14 video time, video is from before UEFN release and has many predictions</sub>

#### Official materials:
 * ▶[2020 Year In Review | Inside Unreal (reveal of Verse scripting language)](https://youtu.be/pjK6QHlbfKE?t=3632) <sub>at 1:00:45 video time. Dec 2020</sub>
 * ▶ **[The Verse programming language GDC 2023](https://youtu.be/teTroOAGZjM?t=22494)**
-------------

# 💚 Visual Verse - visual scripting language developed by Epic
**Epic is working on visual scripting language and Unreal Engine IDE for it and to be used potentially in UEFN/Fortnite**

<details>

***<summary>🟢 Visual Verse - what we know alreadyc</summary>***

-------------
 ## Epic is working on ***[Visual Verse](https://twitter.com/UnrealVerseGuru/status/1636691915927171072)*** visual scripting language
  * Visual scripting is a process of using a visual programming language to create computer programs/scripts. Instead of writing lines of code You use GUI elements, connecting nodes/blocks defining behaviour & logic (Unreal Engine uses **Blueprints** (old Kismet) visual scripting language heavily in UE editor for most of in editor avilable tasks & scripting logic)
  * there are not much informations about it beside registering trademark, recruitment posts for Fortnite (probably UEFN) [1](https://twitter.com/UnrealVerseGuru/status/1582139223355768832) [2](https://twitter.com/UnrealVerseGuru/status/1593014047091351552), and some minor mentions/leaks related to it
   * From those we know IDE for Unreal Engine for VV is in the works
 
 -------------
</details>


-------------

# 💜 VC - Verse Calculus
**New Core Calculus for Functional Logic Programming**

Called "CoreVerse" by SPJ "analogy: [Lambda Calculus](https://en.wikipedia.org/wiki/Lambda_calculus)" but made for Verse and FLP languages
#### Official materials:
[1📝]: *[The Verse Calculus: a Core Calculus for Functional Logic Programming](https://simon.peytonjones.org/assets/pdfs/verse-March23.pdf)*

-------------
> #### repo: [VC_VerseCalculusNotes](https://github.com/UnrealVerseGuru/VC_VerseCalculus) contains notes from [1📝] *WIP*



-------------
###### Other Verse related works:

* <sub> [miniVerse](https://github.com/gregr/experiments/tree/master/verse) Attempt adhering to VC rewrite semantics with runnable examples from [1📝] written in authors miniVerse notation </sub>

<sub> This repo is not endorsed by Epic Games, Inc. I'm not Epic Games employee. Made solely for learning and knowledge sharing</sub>
