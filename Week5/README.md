# Monday
* #### Find The Missing Letter
```javascript
function findMissingLetter(array)
{
  let returnValue = ''
  array.reduce((prev, curr) => {
    if(curr.charCodeAt(0) - prev.charCodeAt(0) === 2){
      returnValue = String.fromCharCode(curr.charCodeAt(0) - 1)
    }
    return curr
  })
  return returnValue;
}
```
* #### Reverse Or Rotate?
```javascript
function revrot(str, sz) {
  if (sz <= 0 || str.length == 0 || sz > str.length) return ''
  let chunks = str.match(new RegExp('.{1,' + sz + '}', 'g'));
  return chunks
    .filter(chunk => chunk.length >= sz)
    .map(chunk => {
      let sum = Array.from(chunk).map(value => value ** 3).reduce((prev, curr) => prev + curr)
      if(sum % 2 === 0){
        return Array.from(chunk).reverse()
      }
      let arr = Array.from(chunk)
      arr.push(arr.shift())
      return arr
    }).flat().join('')
}
```
# Tuesday
* #### TypeScript Object Type
```typescript
export type User = {
    name: string,
    age: number,
    occupation: string
};

export const users: User[] = [
    {
        name: 'Max Mustermann',
        age: 25,
        occupation: 'Chimney sweep'
    },
    {
        name: 'Kate Müller',
        age: 23,
        occupation: 'Astronaut'
    }
];

export function logPerson(user: User) {
    console.log(` - ${user.name}, ${user.age}`);
}

console.log('Users:');
users.forEach(logPerson);
```
* #### TypeScript Unions
```typescript
interface User {
    name: string;
    age: number;
    occupation: string;
}

interface Admin {
    name: string;
    age: number;
    role: string;
}

export type Person = User | Admin;

export const persons: Person[] /* <- Person[] */ = [
    {
        name: 'Max Mustermann',
        age: 25,
        occupation: 'Chimney sweep'
    },
    {
        name: 'Jane Doe',
        age: 32,
        role: 'Administrator'
    },
    {
        name: 'Kate Müller',
        age: 23,
        occupation: 'Astronaut'
    },
    {
        name: 'Bruce Willis',
        age: 64,
        role: 'World saver'
    }
];

export function logPerson(user: Person) {
    console.log(` - ${user.name}, ${user.age}`);
}

persons.forEach(logPerson);
```
