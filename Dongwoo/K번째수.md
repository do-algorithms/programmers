

```js
function solution(array, commands) {
  return commands.map(val => {
    return array.slice(val[0] - 1, val[1]).sort((a, b) => {
      return a - b
    })[val[2] - 1]
  })
}
```

