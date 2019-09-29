
# Comparing objects

```javascript
const obj1 = {
  name: 'Abdul',
  language: 'js'
}
const obj2 = {
  name: 'Abdul',
  language: 'js'
}
const obj3 = {
  language: 'js',
  name: 'Abdul'
}
```

Considering both objects above, Objects are usually compared by reference in javascript, so

```javascript
obj1 == obj2 //false
```

## To compare both objects

```javascript
JSON.stringify(obj1) == JSON.stringify(obj2) //true
```

Comparing objects using *JSON.stringify()* only works when both objects have the same order, so

```javascript
JSON.stringify(obj1) == JSON.stringify(obj3) //false
```

Check out [Samatha Mings](https://github.com/samanthaming) post on how to [compare objects in javascript](https://www.samanthaming.com/tidbits/33-how-to-compare-2-objects)
