How to use syntax highlighting with the GNU nano text editor
---

#### Files to edit
You can edit the file `/etc/nanorc` or the file `~/.nanorc` to add some syntax for the files that you want.

#### Explaining how syntax highlight work
You first need to specify a line with the name of the syntax and the files that you want to be highlighted by your syntax. Adding a line like :

```
syntax "c-file" "\.(c|h)$"
```
means that you want all the .c and .h files to be highlighted with the content that you specify after this line, with some **regular expressions**. For example, add the following line after the previous line to highlight all the integer numbers (positive or negative) in red :

```
color red "\<[-+]?([1-9][0-9]*|0)?\>"
```

#### Pre made nanorc fileEdit
This file text should be placed into a file named `/etc/nanorc`. If you are not root, then into `~/.nanorc`.

It will enable colors for various type files.


Highlighting Colors and Syntax
---

```
color fgcolor,bgcolor regex
```
For the currently defined syntax, display all expressions matching the extended regular expression regex with foreground color fgcolor and background color bgcolor, at least one of which must be specified. Legal colors for foreground and background color are: **white, black, red, blue, green, yellow, magenta,** and **cyan**. You may use the prefix "**bright**" to force a stronger color highlight for the foreground. If your terminal supports transparency, not specifying a bgcolor tells nano to attempt to use a transparent background.
