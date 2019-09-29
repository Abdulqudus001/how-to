
# How to remove duplicates from an array

## Using forEach

```javascript
const arr = ['John', 'Paul', 'George', 'Paul', 'Ringo', 'John'];
const removeDuplicates = (arr) => {
  let unique = {};
  arr.forEach(item => {
    if(!unique[item]) {
      unique[item] = true;
    }
  });
  return Object.keys(unique);
}
removeDuplicates(arr); // 'John', 'Paul', 'George', 'Ringo'
```

## Using filter

```javascript
const arr = ['John', 'Paul', 'George', 'Paul', 'Ringo', 'John'];
const filter = (arr) => {
  return arr.filter((item, index) => arr.indexOf(item) === index);
}
filter(arr); // 'John', 'Paul', 'George', 'Ringo'
```

## Using set

```javascript
const arr = ['John', 'Paul', 'George', 'Paul', 'Ringo', 'John'];
const filteredArr = [...new Set(arr)];
console.log(filteredArr) // 'John', 'Paul', 'George', 'Ringo'
```
