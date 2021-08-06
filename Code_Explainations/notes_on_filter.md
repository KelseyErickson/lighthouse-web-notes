# Notes on Filter Function

```javascript
const without = function (sourceArray, itemsToRemoveArray){
  let outcomeArray = sourceArray.filter(element => !itemsToRemoveArray.includes(element));
  return outcomeArray;
};
```
In above code the element before the => is the element being filtered from the sourceArray. It will loop throught all the elements of the source array.
After the => the we are seeing if the itemsToRemove array includes (this the .includes) the element from the source array.
If it does not( !itemsToRemoveArray) then the element => !itemsToRemoveArray.includes(element) equals true and we keep the element and add it to our outcomeArray. If it is in the itemsToRemoveArray it equals false and then element is removed from the outcomeArray.