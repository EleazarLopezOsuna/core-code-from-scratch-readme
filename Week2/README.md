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
