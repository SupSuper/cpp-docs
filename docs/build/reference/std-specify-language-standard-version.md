---
title: "-std (Specify Language Standard Version) | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "/std"
  - "-std"
  - "VC.Project.VCCLCompilerTool.CppLanguageStandard"
dev_langs: 
  - "C++"
ms.assetid: 0acb74ba-1aa8-4c05-b96c-682988dc19bd
caps.latest.revision: 5
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
---
# /std (Specify Language Standard Version)
Enable supported C++ language features from the specified version of the C++ language standard.  
  
## Syntax  
  
```  
/std:[c++14|c++17|c++latest]  
```  
  
## Remarks  
  
The **/std** option is used to control the version-specific ISO C++ programming language standard features enabled during compilation of your code. This option allows you to disable support for certain new language and library features that may break your existing code that conforms to a particular version of the language standard. By default, **/std:c++14** is specified, which disables language and standard library features found in later versions of the C++ language standard. To explicitly enable the latest supported compiler and standard library features, use **/std:c++latest**.  
  
The default **/std:c++14** option enables the set of C++14 features implemented by the Visual C++ compiler. This option disables compiler and standard library support for features that are changed or new in more recent versions of the language standard, with the exception of some C++17 features already implemented in previous releases of the Visual C++ compiler. To avoid breaking changes for users who have already taken dependencies on the features available as of Visual Studio 2015 Update 2, these features remain enabled when the **/std:c++14** option is specified:  
  
-   [Rules for auto with braced-init-lists](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n3922.html)  
  
-   [typename in template template-parameters](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n4051.html)  
  
-   [Removing trigraphs](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n4086.html)  
  
-   [Attributes for namespaces and enumerators](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n4266.html)  
  
-   [u8 character literals](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n4267.html)  
  
For additional information on which C++17 features are enabled when **/std:c++14** is specified, see the notes in [Visual C++ Language Conformance](../../visual-cpp-language-conformance.md).
  
The **/std:c++17** option enables the set of C++17 features implemented by the Visual C++ compiler. This option disables compiler and standard library support for features that are changed or new in more recent versions of the Working Draft and defect updates of the C++ Standard.  
  
The **/std:c++latest** option enables the set of C++ language and library features implemented by Visual C++ to track the most recent Working Draft and defect updates of the C++ Standard. Use this switch to get the latest language features supported by the compiler. For a list of supported language and library features, see [What's New for Visual C++](../../what-s-new-for-visual-cpp-in-visual-studio.md). The **/std:c++latest** option does not enable features guarded by the **/experimental** switch.  
  
The **/std:c++14** and **/std:c++latest** options are available beginning in Visual C++ 2015 Update 3. The **/std:c++17** option is available beginning in Visual C++ 2017 Update Version 15.3.  
  
> [!NOTE]
>  Depending on the Visual C++ compiler version or update level, certain C++14 features may not be fully implemented or fully conformant when you specify the **/std:c++14** option. For example, the Visual C++ 2017 RTM compiler does not fully support C++14-conformant `constexpr`, expression SFINAE, or 2-phase name lookup. For an overview of C++ language conformance in Visual C++, see [Visual C++ Language Conformance](../../visual-cpp-language-conformance.md). 
  
### To set this compiler option in the Visual Studio development environment  
  
1.  Open the project's **Property Pages** dialog box. For details, see [Working with Project Properties](../../ide/working-with-project-properties.md).  
  
2.  Select **Configuration Properties**, **C/C++**, **Language**.  
  
3.  In **C++ Language Standard**, choose the language standard to support from the dropdown control, then choose **OK** or **Apply** to save your changes.  
  
## See Also  
  
[Compiler Options](../../build/reference/compiler-options.md)   
[Setting Compiler Options](../../build/reference/setting-compiler-options.md)  
