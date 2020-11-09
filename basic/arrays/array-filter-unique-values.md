## Unique Values (Filter)
> return New Array() | .filter(value, index, self) 

#### Classic | ES5
```js
function onlyUnique(value, index, self) {
  return self.indexOf(value) === index;
}
// usage example:
var a = ['a', 1, 'a', 2, '1'];
var unique = a.filter(onlyUnique);
console.log(unique); 
// unique ['a', 1, 2, '1']
```

#### Best | ES6

```js
const myArray = ['a', 1, 'a', 2, '1'];
let unique = myArray.filter((value, index, self) => self.indexOf(value) === index);
console.log(unique); 
// unique is ['a', 1, 2, '1']
```

#### Fast

> ES6 has a native object Set to store unique values. To get an array with unique values you could do now this:

```js
var myArray = ['a', 1, 'a', 2, '1'];
let unique = [...new Set(myArray)];
console.log(unique); 
// unique ['a', 1, 2, '1']
```

Array.from() / A copy array

```js
var items = [4,5,4,6,3,4,5,2,23,1,4,4,4];
var uniqueItems = Array.from(new Set(items));
console.log(uniqueItens);
// [4,5,6,3,2,23,1]
```