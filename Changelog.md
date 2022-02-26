## CHANGELOG

**v1.1.8**

- Add support for multiple variables declaration (Experimental)
- Fix auto format: new indent level are introduced when macros end with `\` 
- Fix auto format: new lines are introduced in program clourse
- Fix auto format: mins sybmols are incorrect in scome scenarios


**v1.1.7**

- Add local package support
- Add vfxshader support (Experimental)
- Add VS2022 support
- Improve shader script templates workflow
- Fix block comment format issue
- Fix Undo and Save On Format conflicts

**v1.1.6**

- Add format on save feature. Enable it by set `Auto Format On Save` to `true` in options, the default value is `false` for this config item
- Add scripts template feature. We can add customize script template and create them via menu `Create -> Shader -> [Customize Name]`. Install/update them to Unity by the menu `Tools -> ShaderlabVS Pro -> Install Script Templates` and Restart Unity is required
- Fix include files seaching is sometimes not working on old or upgraded Unity Project
- Fix bug for formatting '--1' with wrong result


**v1.1.5**

- Add more built in shader libaries
- Fix comment result will not correct in some scenarios
- Fix that macros contains brace get wrong results in auto format

**v1.1.4**

- Improve performance for ASE shaders

**v1.1.3**

- Improve supports for shaders inside Packages folders

**v1.1.2**

- Add supports for shaders inside Packages folder
- Add supports for Visual Studio 2020 Preview
- Fix bug that some fields of struct are missing in code completion when struct contains macros
- Fix minor bugs in auto format

**v1.1.1**

- Improve macros formatting in AutoFormat
- Fix exception when `place brace in new line` is `false` in Auto Format
- Fix bug that code completion of struct with method members is not correct

**v1.1.0**

- Add `Format Selection` feature
- Better HLSL Supports that add more keywords and builtin methods
- Better Outlining that support regions and program blocks
- Better macros formatting. We can change different styles in `Macros Alignment Modes` settings
- Better Syntax highlighting for types and methods
- Fix bugs that StructuredBuffer show as Buffer type in hover information
- Fix some formatting bugs that breaking shader compile

**v1.0.5**

* Better code completion match
* Add version update notification
* Fix some minor bugs

**V1.0.4**

* Improve highlighting for all occurrences will ignore comment line
* Improve performance for large files
* Fix bug that highlighting is not work for last comment line of code

**V1.0.3**

* Add `placing open brace on new line` formatting style
* Add type info in hover information
* Fix bug that variables in method cannot found in `Go To Definition`
* Fix type name is wrong for some variables/members in some scenarios

**V1.0.2 Beta3**

- Add `Go To Definition` features for methods/variables/types
- Add highlighting for all occurrences for selected word
- Add signature help support for method defined by macros
- Improve brace match marker background color 
- Fix bug that method defined by macros are missing in completion
- Fix bug that duplicated completion item in Code Complete
- Fix bug that built-in included shader libraries are missing

**V1.0.1 beta2**

- Improve syntax highlighting
- Add code snippets support

**v1.0 beta1**

init commit