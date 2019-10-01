
# How to sort array of objects

```javascript
/**
 * Sorts an array of objects
 * @param {object} array The array to be sorted
 * @param {string} sortby The parameter to sort the array with
 * @returns {object} Returns the sorted array
 */
function sortBy (array, sortby) {
  function _compare(a,b) {
    if (a[sortby] < b[sortby])
      return -1;
    if (a[sortby] > b[sortby])
      return 1;
    return 0;
  }
 array.sort(_compare);
 return array;
}
```

The function sortBy takes in two parameters, **array**, which is the array of objects, and **sortBy**, which is the key you want to use a base for sorting. Given the following array of objects, to be sorted by name:

```javascript
const arrOfObj = [
  {
    name: 'John',
    language: 'javascript'
  },
  {
    name: 'Jane',
    language: 'python'
  },
  {
    name: 'Doe'
    language: 'rails',
  },
]
sortBy(arrOfObj, 'name'); // Returns the array with Doe, Jane and the John
```
