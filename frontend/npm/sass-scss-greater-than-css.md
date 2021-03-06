# SASS / SCSS -&gt; CSS

## Also, check out CSS-Modules. No compilation necessary:

[https://glenmaddern.com/articles/css-modules](https://glenmaddern.com/articles/css-modules)

## npm run scss

{% embed url="https://sunlightmedia.org/sass/" %}

Also includes nice lesson about SCSS/SASS. Skip toward the bottom. Package.json scripts:  
`"scss": "node-sass -w assets/scss -o assets/css"` 

"-o" flag means "--output".   
"-w" flag means "--watch" for changes, remove for production build.

#### So, instead of importing the SCSS file, link the CSS in the html:

```text
<link rel="stylesheet" type="text/css" href="/css/compiled.css"/>
```

run the SCSS -&gt; CSS compilation before every build:

```text
"dev": "npm run scss:dev && ...your dev script here...",
"build": "npm run scss:pro && ...your build script here...",
"scss:pro": "node-sass ./src/scss -o ./static/css",
"scss:dev": "node-sass -w ./src/scss -o ./static/css",
```

 

