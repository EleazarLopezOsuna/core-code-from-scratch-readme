# Tuesday
* #### Multiply

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
