## CHANGELOG

## Version 1.4.0

**NEW:**
- Able to trigger completion list press `CTRL` + `SPACE` or `CTRL` + `J` which base on keyboard settings

**IMPROVE:**
- Improve tag completion logic, it's more easier to trigger completion list by trigger char `"` and `=` now

**FIX:**
- Fix some bugs in auto format

## Version 1.3.8

**NEW:**
- Add support for methods in structs for Signature Help and hover information
- Add support for methods of Shader Model 5 Objects [Expiremental]
- Add keyword `globallycoherent`
- Add more keywords for BetterShaders

**FIX:**
- Fix extra space will add to '?:' after auto-format
- Fix Code completion items will duplicated or missing when structs have overloaded methods

## Version 1.3.2

**NEW:**
- **BetterShaders Support (Experimental)**
    - Add Syntax Highlighting support
    - Add Outline support
    - Add Signature Help support
    - Add Auto Format support
    - Add part of GoToDefinition support

## Version 1.3.1

**NEW:**
- Add static methods support for code completion
- Add Property Drawers supports

**FIXED:**
- Fix include files in HLSLINCLUDE/CGINCLUDE block are ignored

## Version 1.3.0

**NEW:**
- Add Doc Comment feature. Doc comments are the comments start with `///`. Hover Information and Signature Help will display doc comments as documentation
- Add NavigateTo feature support for current document. Shortcut is `Ctrl + ,`

**FIXED:**
- Fix fields of types are not correct in some case
- Fix ?: format is not correct in some case
- Fix completion for RequireOptions tag

### Version 1.2.5

**NEW:**
- Add support for instance methods of struct
- Add support for Local packages which are binplaced under project root path

**IMPROVE:**
- Improve accuracy and speed of Go To Definition
- Improve accuracy and speed of Code Completion

**FIXED:**
- Fix number 2.0 or 3.0 input will be broken when toogle completion mode is on
- Fix Go To Definition doesn't work when mulitple files included in some cases
- Fix typo `multi_compile`

### Version 1.2.0

**NEW:**
- Add Toggle Completion Mode support for space, `.` and ';'. Toggle the settings by menu Edit -> Intellisense -> Toggle Completion Mode (Experimental)

**FIXED:**
- Fix signature help does not work when there are spaces between method name and brackets
- Fix new version notification are not working in some cases

### Version 1.1.8

**NEW:**
- Add support for multiple variables declaration (Experimental)

**FIXED:**
- Fix auto format: new indent level are introduced when macros end with `\` 
- Fix auto format: new lines are introduced in program clourse
- Fix auto format: mins sybmols are incorrect in scome scenarios


### Version 1.1.7

**NEW:**
- Add local package support
- Add vfxshader support (Experimental)
- Add VS2022 support

**IMPROVED:**
- Improve shader script templates workflow

**FIXED:**
- Fix block comment format issue
- Fix Undo and Save On Format conflicts

### Version 1.1.6

**NEW:**
- Add format on save feature. Enable it by set `Auto Format On Save` to `true` in options, the default value is `false` for this config item
- Add scripts template feature. We can add customize script template and create them via menu `Create -> Shader -> [Customize Name]`. Install/update them to Unity by the menu `Tools -> ShaderlabVS Pro -> Install Script Templates` and Restart Unity is required

**FIXED:**
- Fix include files seaching is sometimes not working on old or upgraded Unity Project
- Fix bug for formatting '--1' with wrong result


### Version v1.1.5

**NEW:**
- Add more built in shader libaries

**FIXED:**
- Fix comment result will not correct in some scenarios
- Fix that macros contains brace get wrong results in auto format

### Version 1.1.4

**IMPROVED:**
- Improve performance for ASE shaders

### Version 1.1.3

**IMPROVED:**
- Improve supports for shaders inside Packages folders

### Version 1.1.2

**NEW:**
- Add supports for shaders inside Packages folder
- Add supports for Visual Studio 2020 Preview

**FIXED:**
- Fix bug that some fields of struct are missing in code completion when struct contains macros
- Fix minor bugs in auto format

### Version 1.1.1

**IMPROVED:**
- Improve macros formatting in AutoFormat

**FIXED:**
- Fix exception when `place brace in new line` is `false` in Auto Format
- Fix bug that code completion of struct with method members is not correct

### Version 1.1.0

**NEW:**
- Add `Format Selection` feature

**IMPROVED:**
- Better HLSL Supports that add more keywords and builtin methods
- Better Outlining that support regions and program blocks
- Better macros formatting. We can change different styles in `Macros Alignment Modes` settings
- Better Syntax highlighting for types and methods

**FIXED:**
- Fix bugs that StructuredBuffer show as Buffer type in hover information
- Fix some formatting bugs that breaking shader compile

### Version 1.0.5

**NEW:**
* Add version update notification

**IMPROVED:**
* Better code completion match

**FIXED:**
* Fix some minor bugs

### Version 1.0.4

**IMPROVED:**
* Improve highlighting for all occurrences will ignore comment line
* Improve performance for large files

**FIXED:**
* Fix bug that highlighting is not work for last comment line of code

### Version 1.0.3

**NEW:**
* Add `placing open brace on new line` formatting style
* Add type info in hover information

**FIXED:**
* Fix bug that variables in method cannot found in `Go To Definition`
* Fix type name is wrong for some variables/members in some scenarios

### Version 1.0.2 Beta3

**NEW:**
- Add `Go To Definition` features for methods/variables/types
- Add highlighting for all occurrences for selected word
- Add signature help support for method defined by macros

**IMPROVED:**
- Improve brace match marker background color 

**FIXED:**
- Fix bug that method defined by macros are missing in completion
- Fix bug that duplicated completion item in Code Complete
- Fix bug that built-in included shader libraries are missing

### Version 1.0.1 beta2

**NEW:**
- Add code snippets support

**IMPROVED:**
- Improve syntax highlighting

### Version 1.0 beta1

init commit