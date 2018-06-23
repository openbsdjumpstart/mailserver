# Coding

This document gives a suggestion on how to organize your source code if
you like to contribute to the project.

[Section "Howto"](#howto) gives some general suggestions for writing shell
scripts. And also suggestions for tis project.

[Section "Style Guide"](#style-guide) gives suggestions on how to format your source
code. Because we think it´s important for readability to use a style
consistently within a project.

> Shell scripting is very sensible as it is full of tricks and
> unexpected and difficult to diagnose quirks. At least if you follow
> the same style all the time you should only fall for each trick once.


## Howto

### General

- **Prefer builtins** over external commands. But...(see next)...

- **Use fast external commands** to process very large inputs. Avoid
  unnecessary subshells and pipelines.

- Use functions to improve readability and control scope.


### Project specific

- **Errorhandling:** Use the `err()` function for displaying
  errormessages. Example: `err "some error occured"`
  This function returns 1 or an optional code: `err "some error
  occured" 5`


## Style Guide

- [Lines](#lines)
- [Indentation](#indenting)
- [Tabs, Spaces](#tabs-spaces)
- [Braces](#braces)
- Object names
  - [Variables](#variable-names)
  - [Functions](#function-names)


### Lines

- Prefer lines of **72 characters of length** or less.

  > If you are using vim(1) you can set the width of lines with `set
    textwidth=72`

- Break longer lines by quoting the line ending and stripping the
  newline to split into multiple subsequent lines of no more than 72
  characters each.

  Examples:
  ```
  echo "very_long_string \
        continuation"
  ```

  ```
  command1 \
    | command4 \
    long_argument_list
  ```

- Avoid more than one statement per line.

- Add **blank lines** to improve readability and to indicate
  related blocks of code.

- No trailing whitespace at the end of non-blank lines.


### Indenting

Indent your code by **2 spaces**

> If you are using vim(1) you can set the width of lines with `set
  tabstop=2` and `set softtabstop=2`


### Tabs, Spaces

- **Don´t use tabs** for displaying messages. Expand tabs to spaces.

- **Don´t use tabs** for indenting. Expand tabs to spaces.

- **Don´t use tabs** for anything. Expand tabs to spaces.

> If you are using vim(1) you can set the width of lines with `set
  expandtab`



### Braces

For embracing we are using the Allman Style.
This style puts the brace associated with a control statement on the
next line, indented to the same level as the control statement.
Statements within the braces are indented to the next level.

Example:
```
function()
{
  something
  somethingelse
}
finalthing
```


## Variable names

- A variable is named **according to its scope.**

- **Variablenames** are written lowercase.

- If the variable is **read-only** the name is UPPERCASE.

- **Local** variables are prefixed with an underscore

  Example:
  ```
  local _foo="bar"
  ```

## Function names

- Use underscore to glue verbs and nouns. Don't use camel case or
  hungarian or something.

  Example: Don´t use `InstallAll()` use `install_all()` instead.


