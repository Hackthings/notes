# loops

To remove items from the array, while you're looping over the array, without breaking the current index:

```text
let i = 0;
while (i < list.length) { // new length read and compared to i each time

   if (...something...) {

      list.splice(i, 1); // if delete an item then don't increment index

   } else {

      i++; // if length did not change, then increment indes like normal

   }
}
```

 

