# Wednesday
* #### Simple Validation Of A Username
```javascript
function validateUsr(username) {
  return /^([a-z0-9_]){4,16}$/.test(username) 
}
```
* #### Get Number From String
```javascript
function getNumberFromString(s) {
  return Number(s.replace(/\D/g, ''));
}
```
# Thursday
* #### String Cleaning
```javascript
function stringClean(s){
  return s.replace(/\d/g, '');
}
```
* #### Password Validation
```javascript
function validate(password) {
  return /^[A-Za-z0-9]{6,}$/.test(password) && /[A-Z]+/.test(password) && /[a-z]+/.test(password) && /[0-9]+/.test(password)
}
```
