ShaderlabVS Pro
====

##  Introduction

ShaderlabVS Pro is a Visual Studio plugin for Unity shaderlab programming. It is paid version of [ShaderlabVS](https://github.com/wudixiaop/ShaderlabVS) which I made and open source since the year 2014. Compared with ShaderlabVS, it has more features and better performance.

<p>
<a href='http://forum.unity3d.com/threads/1032139/' target='_blank'><strong>Forum</strong> </a> | 
<a href='mailto:amlovey@qq.com'><strong>Email</strong></a> |
<a href='https://assetstore.unity.com/packages/slug/186176?aid=1011lGoJ' target='_blank'><strong>Purchase On Asset Store</strong> </a>  |
<a href='https://mianbaoduo.com/o/bread/Zpubmpg=' target='_blank'><strong>Purchase On MianBaoDuo</strong></a>
</p>

![](http://www.amlovey.com/shaderlabvs/assets/Overview.png)

## Installation

1. Get .vsxi file under path `Assets/ShaderlabVS/VSPlugin`
2. Double click the .vsxi file, a Visual Studio extension install window will pop up
3. Click `Install` button on install the window 
4. After install successfully, restart Visual Studio

## Support Visual Studio Version

-  Visual Studio 2019
-  Visual Studio 2022 Preview

## Main Features

### Syntax Highlighting

![](http://www.amlovey.com/shaderlabvs/assets/DarkTheme.png)

### Code Completion and Basic Intellisense

![](http://www.amlovey.com/shaderlabvs/assets/MemeberIntelisense.png)

### Hover Information

![](http://www.amlovey.com/shaderlabvs/assets/HoverInformation.png)

### Signature Help

![](http://www.amlovey.com/shaderlabvs/assets/SignatureHelp.png)

### Auto Format

#### Format Document

via menu `Editor -> Advanced -> Format Document` 

#### Format Selection



#### Place Open Brace On New Line

We can set brace formatting style in **Tools** -> **Options** -> **Text** **Editors** -> **Shaderlab** -> **Formatting** page.

If `Place Open Brace On New Line` is `true`, after formatting, open brace will be in new line, like below

```csharp
if (true)
{
  
}
```



if `Place Brace On New Line` is `fase`, after formatting, open brace will not in new line.

```csharp
if (true) {
  
}
```
#### Macros Alignment Modes

In Settings, there is an item under `ShaderlabVScode` section named `Formatting: Style`, change the `Macros alignment modes` to set formatting mode for macros.

##### Indentation with hierachy

```csharp
Subshader 
{
    Pass
    {
        CGPROGRAM
        void MacroTest()
        {
            float c;
            #if 0
                c = 0;
                #if 1
                    c = 1;
                #endif
            #endif
        }
        ENDCG
    }
}
```

##### Indentation without hierachy

```csharp
Subshader 
{
    Pass
    {
        CGPROGRAM
        void MacroTest()
        {
            float c;
         #if 0
                c = 0;
         #if 1
                c = 1;
         #endif
         #endif
        }
        ENDCG
    }
}
```

##### No Indentation but with hierachy

```csharp
Subshader 
{
    Pass
    {
        CGPROGRAM
        void MacroTest()
        {
            float c;
#if 0
            c = 0;
    #if 1
            c = 1;
    #endif
#endif
        }
        ENDCG
    }
}
```

##### No Indentation and without hierachy

```csharp
Subshader 
{
    Pass
    {
        CGPROGRAM
        void MacroTest()
        {
            float c;
#if 0
            c = 0;
#if 1
            c = 1;
#endif
#endif
        }
        ENDCG
    }
}
```



### Go To Definition

![](http://www.amlovey.com/shaderlabvs/assets/GoToDefinition.png)

### Support SRP

![](http://www.amlovey.com/shaderlabvs/assets/SRP.png)

### Code Snippets
Below are the snippets:

| Snippets     | Description                                           |
| ------------ | :---------------------------------------------------- |
| blend1-dc_1  | Blend OneMinusDstColor One                            |
| blend1_1-sa  | Blend One OneMinusSrcAlpha                            |
| blend1_1     | Blend One One                                         |
| blenddc_0    | Blend DstColor Zero                                   |
| blenddc_sc   | Blend DstColor SrcColor                               |
| blendsa_1-sa | Blend SrcAlpha OneMinusSrcAlpha                       |
| cgp          | CGPROGRAM...ENCG                                      |
| for          | `for` loop                                            |
| forr         | Reverse `for` loop                                    |
| glp          | GLSLPROGRAM...ENCGLSL                                 |
| hlp          | HLSLPROGRAM...ENDHLSL                                 |
| if           | if { ... }                                            |
| ifelse       | if {...} else {...}                                   |
| inc          | #include ""                                           |
| incpkg       | #include "Packages"                                   |
| incucg       | #include "UnityCG.cginc"                              |
| prop2d       | `2D` type property                                    |
| propc        | `Color` type property                                 |
| propcube     | `Cube` type property                                  |
| propf        | `Float` type property                                 |
| proprange    | `Range` type proprety                                 |
| props        | Properties { ... }                                    |
| propv        | `Vector` type property                                |
| shader       | Shader { ... }                                        |
| struct       | struct { ... };                                       |
| subshader    | SubShader { ... }                                     |
| tags         | Tags { ... }                                          |
| tagtt        | Tags with both of RenderType and Queue is Transparent |

## Support Visual Studio Version

- Visual Studio 2019

## Support Files

* .shader
* .cginc
* .glslinc
* .compute
* .cg
* .hlsl

## CHANGELOG

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
