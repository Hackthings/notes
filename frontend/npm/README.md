# npm

### No more \`../../../\` hell! :\)

When importing something from the current folder, or a child folder, it makes sense to use a path relative to the current file:  
`import something from "./file.html"`

But when importing from outside the folder, or somewhere else in the codebase, using relative paths is very messy! It ends up being different in every module, and very confusing to read and understand what file it's referring to. Sure, a good IDE can solve this, but I see this excuse too often. We shouldn't rely on the IDE for every little thing. What if you're using some new unfamiliar IDE? What if your IDE starts acting up and no longer reformats the paths correctly? It happens all the time. If I can help it, I avoid things which make my code tedious and convoluted.  
`import something from "../../../../path/to/file.html"`, 

### Just do this:

It makes refactoring and renaming so much easier!  
`import something from "src/path/to/file.html"` 

### This is very easy to enable:

1. Add a `package.json` file to the `/src` folder, containing this:

   ```text
   {
     "name": "src",
     "description": "Local module, import as a node module path. Install with `npm link ./path/to/here`"
   } 
   ```

2. Run `npm install ./src` . That's it. Now you can refer to your "src" folder as if it was a module, because now it is a module! :\) 



