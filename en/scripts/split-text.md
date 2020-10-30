---
title: Split text into an array of strings
desc: The command splits the text into an array of lines and assigns it to an object variable.
img:
   split-text: scripts/split-text.png
html:
   split-text: '<img src="%img.split-text%" style="margin: 1em 1em;"/>'
---
# Split Text

The **Split Text** command splits the text into substrings separated by a separator string and saves the array of strings to an object variable.

%html.split-text%

**Text**  
Specify the source text to be split. Below are several options for the definition of this parameter.

``` txt
First line
Second line
```

``` txt
#myvalue#
```

``` txt
</home/user/data/data.txt>
```

**Delimiter**  
Specify a string that will be the separator for substrings. Specify *#.n#* for line feeds, *#.s#* for the space.

**Result variable**  
Specify the name of the object variable to which the resulting array of substrings will be assigned.
