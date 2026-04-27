# DevTools Part 2

1. The bug was that `num1` and `num2` were read from the input fields as strings. Because of this, the `+` operator joined them together as text instead of adding them as numbers. For example, `2` and `3` became `23`.

2. I would fix it by converting `num1` and `num2` into numbers before adding them:

```js
let result = Number(num1) + Number(num2);