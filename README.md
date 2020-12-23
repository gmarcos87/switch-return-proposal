# Switch return

## The Problem
Nested if statements to define a constant
```js
const colorIf = type === 'apple'
  ? 'red'
  : type == 'banana'
    ? 'yellow'
    : 'invisible'
```


```js
const colorSwith = ((t) => {
  switch(t) {
    case 'apple':
      return 'red'
    case 'banana':
      return 'yellow'
    default
      return 'invisible'
  }
})(type)
```



## Solutions
To be able to use switch as an expression to assign a value.
It could even be used with the implicit return within the cases.

### Syntax

```js
const color = switch(type) {
  case 'apple':
    return 'red'
  case 'banana':
    return 'yellow'
  default
    return 'invisible'
}
```

With implicit return
```js
const color = switch(type) {
  case 'apple':
    'red'
  case 'banana':
    'yellow'
  default
    'invisible'
}
```
