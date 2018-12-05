# C++ Coding Standard

## Introduction

This document describes C++ coding guidelines for projects in the [CodeSmithyIDE organization](https://github.com/CodeSmithyIDE).

## Physical layout of the code

1. Lines shall be no more than 120 characters in length excluding the new line character(s).

    > We exclude the newline character(s) as this gives a round number for the developer to follow. This also removes the need
    > to worry about the number of characters used for the newline depending on the platform.

1. The newline character shall be:
    1. "\r\n" on Microsoft Windows platforms.
    1. "\n" on Unix platforms.

1. Header files shall have a ".h" extension.

1. Source files shall have a ".cpp" extension.

1. Filenames shall use UpperCamelCase with the following modification:

1. Namespaces, class names and function names can be included in the file name and be separated from each other and other parts
   of the file with an underscore.

    Example:\
    If a namespace *TheNameSpace* contains a class called *TheClass*, the file name would be: *TheNameSpace_TheClass*.

    > This rule is for files that do not contain source code as the following rules describe stricter naming conventions for files
    > that contain source code.

1. A header file that contains the declaration of a class shall have the same name as the class.

    Example:\
    If the file contains the declaration for the class *TheClass*, the file shall be named *TheClass.h*.

1. A source file that contains the definition of a class shall have the same name as the header file for that class.

    Example:\
    If the file contains the definition for the class *TheClass*, and assuming that the header file has been named *TheClass.h* as
    per the previous rule, the name of the file shall be *TheClass.cpp*.

    > We link the name of the source file to the name of the header file so that if a case arises where the name of the header file
    > does not follow the rule then at least the header file and source file have the same name.

## Indentation style

9. Indentation shall use 4 spaces and not tabs.

    > We had to choose one or the other.

1. Curly braces shall use the Allman style.

     Example:
     ```
     void Function(bool condition)
     {
         if (condition)
         {
             DoSomething();
         }   
     }
     ```

    > We consider this style to be the most readable and it is common in C++ code.

1. Curly braces shall not be omitted when they contain a single statement.

    Example:
    ```
    if (condition)
    {
        DoSomething();
    }
    ```
    and not
    ```
    if (condition)
        DoSomething()
    ```

    > Omitting the braces leads to subtle errors and breaks consistency.

## Naming conventions

12. Namespace names shall use UpperCamelCase.

    Examples:\
    *Pets*, *FourLeggedAnimals*

1. Class names shall use UpperCamelCase.

    Examples:\
    *TheDog*, *ADog*, *Dog*

1. Non-static method names shall use lowerCamelCase.

    Examples:\
    *barks()*, *playsFetch()*

1. Static method names shall use UpperCamelCase.

    Examples:\
    *StaticBarks()*, *StaticPlaysFetch()*

1. The names of functions that are not part of a class shall use UpperCamelCase.

    Examples:\
    *Function()*, *MyFunction()*

1. Member variable names shall start with "m_" and user lowerCamelCase.

    Examples:\
    *m_name*, *m_bestFriend*

1. Macro names shall use SCREAMING_SNAKE_CASE.

    Examples:\
    *DOG*, *THE_CUTE_DOG*

1. Header guard names shall be formed by:
    1. taking the path of the header file, converting it to upper case and replacing the path separators with underscores,
    1. then prefixing the result of the previous step with the name of the project in upper case followed by an underscore,
    1. and finally adding a leading and a trailing underscore to the result of the previous step.

    Examples:\
    For a header file in a project called *TheProject* that has the path *Dir1/SubDir2/HeaderFile.h*, the header guard shall be named
    *\_THEPROJECT_DIR1_SUBDIR2_HEADERFILE_H\_*. Note that we do not write *SUB_DIR2* but *SUBDIR2*.
