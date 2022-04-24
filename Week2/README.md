# Tuesday
* #### Multiply
```javascript
function multiply(a, b){
  return a * b;
}
```
* #### ASCII Total
```javascript
function uniTotal (string) {
  if(string.length === 0)
    return 0;
  var returnValue = 0;
  for(var i = 0; i < string.length; i++){
    returnValue += string.charCodeAt(i);
  }
  return returnValue;
}
```
* #### Char From ASCII Value
```javascript
var getChar = String.fromCharCode;
```
* #### Binary Addition
```javascript
addBinary = (a, b) => {
  return (a + b).toString(2);
}
```
* #### Student's Final Grade
```javascript
function finalGrade (exam, projects) {
  return (exam > 90 || projects > 10) ? 100 :
  (exam > 75 && projects >= 5) ? 90 :
  (exam > 50 && projects >= 2) ? 75 : 0
}
```
# Wednesday
* #### Holiday VIII - Duty Free
```javascript
function dutyFree(normPrice, discount, hol){
  return Math.floor(hol/(normPrice * (discount/100)))
}
```
* #### Twice As Old
```javascript
function twiceAsOld(dadYearsOld, sonYearsOld) {
  let i = 0
  while(true){
    if((dadYearsOld + i) === 2 * (sonYearsOld + i))
      return i
    if((dadYearsOld - i) === 2 * (sonYearsOld - i))
      return i
    i++
  }
}
```
* #### Valid Spacing
```javascript
function validSpacing(s) {
  const re = new RegExp('\\s\\s+')
  if(s.startsWith(' ') || s.endsWith(' ') || s.match(re))
    return false
  return true
}
```
* #### Fake Binary
```javascript
function fakeBin(x){
  return x.replace(/[0-4]/ig, '0').replace(/[5-9]/ig, '1')
}
```
# Thursday
* #### Remove All Exclamation Marks From The End Of Sentence
```javascript
function remove (string) {  
  if(string.endsWith('!'))
    return remove(string.slice(0, string.length - 1))
  return string
}
```
* #### Vowel Remover
```javascript
function shortcut (string) {
  const vowels = ['a', 'e', 'i', 'o', 'u']
  return Array.from(string).filter(element => {
    return !vowels.includes(element)
  }).join('')
}
```
* #### Rock Paper Scissors! 
```javascript
const rps = (p1, p2) => {
  const draw = 'Draw!'
  const player1 = 'Player 1 won!'
  const player2 = 'Player 2 won!'
  if(p1 === p2)
    return draw
  if(p1.startsWith('s')){
    if(p2.startsWith('p'))
      return player1
    return player2
  }
  if(p1.startsWith('p')){
    if(p2.startsWith('r'))
      return player1
    return player2
  }
  if(p1.startsWith('r')){
    if(p2.startsWith('s'))
      return player1
    return player2
  }
      
};
```
* #### Persistent Bugger
```javascript
function persistence(num) {
  if(num < 10)
    return 0
  return 1 + persistence(
    Number(
      Array.from(
        num.toString()
      ).reduce(
        (previousValue, currentValue) => previousValue * currentValue)
    )
  )
}
```
