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

## Naming conventions

9. Namespaces shall use UpperCamelCase.

    Examples:\
    *Pets*, *FourLeggedAnimals*

9. Class names shall use UpperCamelCase.

    Examples:\
    *TheDog*, *ADog*, *Dog*

9. Method names shall use lowerCamelCase.

    Examples:\
    *barks()*, *playsFetch()*

9. Member variable names shall start with "m_" and user lowerCamelCase.

    Examples:\
    *m_name*, *m_bestFriend*

9. Macro names shall use SCREAMING_SNAKE_CASE.

    Examples:\
    *DOG*, *THE_CUTE_DOG*

9. Header guards shall start and end with an underscore. They shall be formed by concatenating the names
   of the directories and the file name together.

    Examples:\
    For a header file in a project called *TheProject* that has the path *Dir1/SubDir2/HeaderFile.h*, the header guard shall be named
    *\_THEPROJECT_DIR1_SUBDIR2_HEADERFILE_H\_*. Note that 
