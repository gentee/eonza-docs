---
title: Parsing HTML page
desc: The command parses the HTML page.
img:
   parse-html: scripts/parse-html.png
html:
   parse-html: '<img src="%img.parse-html%" style="margin: 1em 1em;"/>'
---
# Parse HTML

**v1.20.0**  
The **Parse HTML** command parses HTML text and retrieves the content or attributes of the selected elements.

%html.parse-html%

**HTML variable or node**  
Specify the name of the variable that contains the text of the HTML page. You can also specify the name of a node that was obtained by another *Parse HTML* command. In this case, parsing will continue inside the specified element.

```txt
htmldata
#htmldata#
</#path#/myfile.html>
```

**Selector**  
Elements selector. To select items, you can use the queries that are accepted in **jQuery**.

* **#myId** - selection of elements by *id*.
* **li a** - selection of elements by tags. In this example, all links that are contained in the *li* tags will be selected.
* **.myClass** - selection of elements by the class name.
* **input[name='firstname']** - selection of elements by attributes.

You can combine selection parameters. For example, *#main ul.list li* will select all tags *li* inside *ul* with class *list* that are located inside element with id equal to *main*.

**Node Name**  
Nested commands will be executed for each selected element. Specify the name of the variable that will contain the current element. In this case, you can use it again in the *Parse HTML* command. Also, you can specify it to get values.

* **#name#** - content will be returned, including children.
* **#name.attrib#** - the value of the specified attribute for the selected element will be returned.

If you need to select only one element and get its text or attributes, then you can omit the *Selector* and *Node Name* parameters, but add queries to the *Selectors* list.

## Selectors

Here you can specify selectors and variable names to get the content of found items.

**Selector**  
Element selection. If several elements are found, only the value of the first found element will be retrieved.
If a node name is specified in the *HTML Variable or Node* parameter, this field can be empty. In this case, the text of the corresponding element will be returned.

**Attribute**  
Specify the name of the attribute whose value you want to get. If not specified, the variable will be assigned
element text.

**Variable name**  
Specify the name of the variable to which the content of the first found element or its attribute value will be assigned.
