# Solution

### Challenge 5: Needle in a Haystack

```js
var findNeedle = haystack => {
    var index = haystack.findIndex(word => word === "needle");
    return `Found the needle at position ${index}`;
}
```