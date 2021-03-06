# WebStorm for Javascript

* It actually indents JSX correctly and reliably! Even Prettier can't indent JSX. Others sometimes totally break it.  
* It allows you to choose your indentation style \(inline, each bracket on its own line\), and lets you use multiple styles in the same project! So, you don't have to have ALL your brackets squished onto one line, or taking up your whole vertical screen each on their own line. You, as the human, may decide if you want a particular block of code squished or expanded.  
* When you rename a file, it can rename all references \(links/imports\) to that file  
* It can do backwards-search easily. Double-click to select some string. `Cmd+F` then `Cmd+Shift+G`. I could not figure out how to do this in Sublime/VsCode, which is how I found this IDE in the first place! 
* Other shortcuts like this are really easy to find, and customize. In its preferences, you can search for a shortcut not just by name, but by actually pressing the key\(s\).
* "Rainbow brackets" is a standard feature, and work really well. Look it up if unfamiliar!
* If you're using 4 spaces for indentation. Other editors will make you delete one at a time for certain file types \(so, press delete 4 times per tab! just use tabs, please!\). WebStorm detects indentation correctly for every file type. Also, by default, when you hit delete on a new indented line, it can delete ALL the indents on that line and the line break, to bring you back to the end of the last line's code.  
* It has ESLINT integrated, and other extras \(like rainbow brackets\) are standard or easy to add. ESLINT alerts you \(with a little underline\) when you're trying to use a variable which is misspelled, or import a file which doesn't exist. Code hints look noticeable but not annoying.  

## It has powerful customizable options for code-formatting,

or you can use the same .prettierrc file as your teammates do with their Sublime/VsCode. Just install the Prettier plugin.

## Get started fast:

[Download my exported settings file](https://github.com/paulshorey/notes/raw/master/files/linked/WebStormSettings.zip), which adds useful shortcuts for people used to Sublime Text or VS Code.

WebStorm lets you search KeyBindings by name, OR by the pressing the keyboard keys and find out what that combination does \(and re-map it to the thing you want it to do\).

Above settings file changes these key bindings, and many others. It also changes the theme/colors and removes unnecessary clutter/menus.

```text
Cmd+D           incremental add selection (multiple cursor)  

Cmd+F           search selection in current document  
Cmd+G           go to next search result  
Cmd+Shift+G     go to previous search result  
Cmd+R           search/replace in current document  
Cmd+Shift+R     when folder selected in nav, search/replace inside it  

Ctrl+R           when file/folder selected in nav, "refactor" rename it  

Cmd+Shift+,     previous file tab  
Cmd+Shift+.     next file tab  

Cmd+Shift+;     previous WebStorm window  
Cmd+Shift+'     next WebStorm window  

Cmd+1           open (or focus on) project file navigation
```

## Gotchas, stuff to remember

besides things fixed by the settings file:

1. By default, WebStorm will not open a file for editing when you simply click once on the file in navigation. You have to double-click to open a file. To make a file opened with one click \(like in Sublime/VsCode\), click the little gear icon in top right Project menu \(file navigation\), and select "Autoscroll to Source". Also check "Autoscroll from Source".  

