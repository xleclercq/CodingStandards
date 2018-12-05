# C++ Coding Standard

## Introduction

This document describes C++ coding guidelines for projects in the [CodeSmithyIDE organization](https://github.com/CodeSmithyIDE).

## Physical layout of the code

1. Lines will be no more than 120 characters in length excluding the new line character(s).
1. The newline character will be:
    1. "\r\n" on Microsoft Windows platforms.
    1. "\n" on Unix platforms.
1. Header files will have a ".h" extension.
1. Source files will have a ".cpp" extension.
1. Filenames will use camel case with the following modification:
1. Namespaces, class names and function names can be included in the file name and be separated from each other and other parts of the file with an underscore.
    Example: if a namespace TheNameSpace contains a class called TheClass, the file name would be TheNameSpace_TheClass.