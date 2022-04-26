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
# Tuesday
* #### Simple Pig Latin
```javascript
function pigIt(str){
  const wordRegex = /[a-zA-Z]+/g;
  var wordsArray = str.split(' ')
  console.log(wordsArray)
  return wordsArray.map(
    function(word){
      if(word.match(wordRegex)){
        return word.substring(1,word.length) + word.charAt(0) + 'ay'
      }
      return word
    }
  ).join(' ')
}
```
* #### Counting Duplicates
```javascript
function duplicateCount(text){
  text = text.toLowerCase()
  var charArray = Array.from(text)
  var charDictionary = {}
  var repeatCount = 0;
  charArray.forEach(char => {
    if(charDictionary.hasOwnProperty(char)){
      charDictionary[char] = charDictionary[char] + 1
      return
    }
    charDictionary[char] = 1
  })
  for (const [key, value] of Object.entries(charDictionary)) {
    if(value > 1){
      repeatCount++
    }
  }
  return repeatCount
}
```
* #### Decode The Morse Code
```javascript
decodeMorse = function(morseCode){
  var wordsArray = morseCode.split('   ')
  return wordsArray.map(word => {
    let charArray = word.split(' ')
    charArray = charArray.map(char => {
      return MORSE_CODE[char]
    })
    return charArray.join('')
  }).join(' ').replace(/^\s*/mg, '')
}
```
# Wednesday
* #### Valid Parentheses
```javascript
```
* #### Convert String To Camel Case
```javascript
```
* #### Unique In Order
```javascript
```
# Thursday
* #### Fold An Array
```javascript
```
* #### Encrypt This!
```javascript
```
