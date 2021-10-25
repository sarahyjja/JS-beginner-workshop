# Solution

### Challenge 4: FizzBuzz

Long solution
```js
var fizzBuzz = n => {
    for(var num = 1; num <= n; num++){
        if(num % 15 === 0){ console.log('FizzBuzz')}
        else if(num % 3 === 0){ console.log('Fizz')}
        else if(num % 5 === 0){ console.log('Buzz')}
        else { console.log(num)}
    }
}
console.log(fizzBuzz(15))
```

Short solution
```js
for(var num = 0; num < 16;) console.log((++num % 3 ? '' : 'fizz') + (num % 5 ? '' : 'buzz') || num)
```