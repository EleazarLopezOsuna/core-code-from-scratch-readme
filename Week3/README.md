# Monday
* #### Who Likes It?
```javascript
function likes(names) {
  if(names.length === 0)
    return 'no one likes this'
  if(names.length === 1)
    return names[0] + ' likes this'
  if(names.length === 2)
    return names[0] + ' and ' + names[1] + ' like this'
  if(names.length === 3)
    return names[0] + ', ' + names[1] + ' and ' + names[2] + ' like this'
  return names[0] + ', ' + names[1] + ' and ' + (names.length - 2) + ' others like this'
}
```
* #### Bit Counting
```javascript
var countBits = function(n) {
  return Array.from(n.toString(2)).filter(value => {
    return Number(value) === 1
  }).length
};
```
* #### Your Order, Please
```javascript
function order(words){
  var dict = {}
  var wordsArray = words.split(' ')

  wordsArray.forEach(word => {
    let number = word.match(/[1-9]/g)
    dict[word] = number
  })

  var items = Object.keys(dict).map(function(key) {
    return [key, dict[key]]
  });

  items.sort(function(first, second) {
    return first[1] - second[1]
  });

  wordsArray = []

  items.forEach(element => {
    wordsArray.push(element[0])
  })

  return wordsArray.join(' ')
}
```
