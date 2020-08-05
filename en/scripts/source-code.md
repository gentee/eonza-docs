---
title: Source Code script
desc: The Source Code allows you to use Gentee programming language in scripts.
img:
   source-code-1: scripts/source-code-1.png
   source-code-2: scripts/source-code-2.png
   source-code-sample-1: scripts/source-code-sample-1.png
   source-code-sample-2: scripts/source-code-sample-2.png
html:
   source-code-1: '<img src="%img.source-code-1%" style="margin: 1em 1em;"/>'
   source-code-2: '<img src="%img.source-code-2%" style="margin: 1em 1em;"/>'
   source-code-sample-1: '<img src="%img.source-code-sample-1%" style="margin: 1em 1em;"/>'
   source-code-sample-2: '<img src="%img.source-code-sample-2%" style="margin: 1em 1em;"/>'
---
# Source Code

The **Source code** script allows you to use the [Gentee script programming language](https://docs.gentee.org) in your scripts.

%html.source-code-1%

**External source code**  
If you mark this checkbox, then define top-level constructs like *func, type, const* in the Source code field. Otherwise, the Source Code field must contain language constructs that can be used inside the function body.

**Source Code**  
You can insert any source code in the Gentee programming language here. Note that the Source command allows you to insert other commands inside itself. In this case, use the **%body%** macro to substitute the internal commands. For example, if we want to execute a set of some commands several times, we can use the Source Code script with the code like the following one. 

``` go
for i in 1..10 {
    SetVar("index", str(i))
    %body%
}
```

%html.source-code-2%

* [%dwnsample%](/samples/source-code-sample.yaml)

%scriptresult%

%html.source-code-sample-1%
%html.source-code-sample-2%
