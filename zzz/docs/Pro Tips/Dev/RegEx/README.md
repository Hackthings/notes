# Regular Expressions  
  
> * **[Basics](./Basics.md)**  
> * **[HTML](./HTML.md)**  
> * **[Javascript](./Javascript.md)**  
> * **[Markdown](./Markdown.md)**  
<br />  
  
Lets use the link above as an example.  
We want to find/replace local links from `.md` to `.html`...  
  
#### in IDE:  
```  
Find: (\[.*?\]\(\./.*?).md(\))  
Replace: $1.html$2  
```  
#### using Javascript:  
```  
str.replace(\(\[.*?\]\(\./.*?).md(\))\g, "$1.html$2");  
```  
<br />  
  
So, no matter the complexity, just write the match/replace as:  
```  
str.replace(\        \g, "       ")  
```  
 