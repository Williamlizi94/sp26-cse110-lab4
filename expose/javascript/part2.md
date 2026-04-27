# Part 2 Answers

1. Line 12 prints `3`. Since `i` is declared with `var`, it has function scope, not block scope. After the loop finishes, `i` is still accessible, and its value is `3`.

2. Line 13 prints `150`. Since `discountedPrice` is declared with `var`, it is function-scoped. After the loop ends, it still exists and stores the last calculated discounted price, which is `300 * 0.5 = 150`.

3. Line 14 prints `150`. Since `finalPrice` is declared outside the loop with `var`, it is function-scoped and still accessible after the loop. Its final value is the last rounded discounted price, which is `150`.

4. The function returns `[50, 100, 150]`. The loop goes through each price, applies the 50% discount, rounds the value, and pushes it into the `discounted` array.

5. Line 12 causes an error. Since `i` is declared with `let` inside the `for` loop, it only exists inside that loop. It cannot be accessed outside the loop.

6. Line 13 causes an error. `discountedPrice` is declared with `let` inside the loop block, so it only exists inside the loop and cannot be accessed at line 13.

7. Line 14 prints `150`. `finalPrice` is declared outside the loop, so it can still be accessed after the loop. Its final value is the last calculated price, which is `150`.

8. The function returns `[50, 100, 150]`. Each price is multiplied by `1 - discount`, so with a discount of `0.5`, each price becomes half of the original price.

9. Line 11 causes an error. The variable `i` was declared with `let` inside the `for` loop, so it only exists inside that loop. It cannot be accessed outside the loop.

10. Line 12 prints `3`. The variable `length` is declared near the top of the function, outside the loop, so it is still accessible at line 12. Since the input array has 3 items, `length` is 3.

11. The function returns `[50, 100, 150]`. The array `discounted` is declared with `const`, but we are not reassigning the array itself. We are only adding values into it with `.push()`, which is allowed.
12.

A. `student.name`

B. `student['Grad Year']`

C. `student.greeting()`

D. `student['Favorite Teacher'].name`

E. `student.courseLoad[0]`
13. Arithmetic

A. `'3' + 2` outputs `'32'`. The `+` operator with a string causes string concatenation, so `2` becomes a string.

B. `'3' - 2` outputs `1`. The `-` operator forces `'3'` to become a number, so it becomes `3 - 2`.

C. `3 + null` outputs `3`. In numeric conversion, `null` becomes `0`.

D. `'3' + null` outputs `'3null'`. Since one side is a string, JavaScript does string concatenation.

E. `true + 3` outputs `4`. `true` converts to `1`, so the result is `1 + 3`.

F. `false + null` outputs `0`. `false` converts to `0`, and `null` also converts to `0`.

G. `'3' + undefined` outputs `'3undefined'`. Since one side is a string, JavaScript concatenates them.

H. `'3' - undefined` outputs `NaN`. The `-` operator tries to convert both sides to numbers, but `undefined` becomes `NaN`.

14. Comparison

A. `'2' > 1` outputs `true`. The string `'2'` is converted to the number `2`, and `2 > 1` is true.

B. `'2' < '12'` outputs `false`. Since both values are strings, JavaScript compares them alphabetically. Since `'2'` comes after `'1'`, the result is false.

C. `2 == '2'` outputs `true`. The `==` operator allows type conversion, so `'2'` becomes `2`.

D. `2 === '2'` outputs `false`. The `===` operator checks both value and type, and one is a number while the other is a string.

E. `true == 2` outputs `false`. `true` converts to `1`, and `1 == 2` is false.

F. `true === Boolean(2)` outputs `true`. `Boolean(2)` becomes `true`, and both sides are booleans with the same value.

15. The `==` operator compares values after allowing type conversion, so values with different types can still be considered equal. The `===` operator compares both value and type, so it is stricter and does not do type conversion. In most cases, `===` is safer to use because it avoids unexpected type conversion.
17. The result is `[2, 4, 6]`. The `modifyArray` function loops through `[1, 2, 3]` and applies the callback function `doSomething` to each value. Since `doSomething` returns `num * 2`, the values become `1 * 2 = 2`, `2 * 2 = 4`, and `3 * 2 = 6`. These new values are pushed into `newArr`, so the function returns `[2, 4, 6]`.
19. The output is:

1
4
3
2

First, `console.log(1)` runs immediately. Then the two `setTimeout` functions are scheduled, but they do not run right away. After that, `console.log(4)` runs immediately. The `setTimeout` with `0` milliseconds runs next and prints `3`. Finally, the `setTimeout` with `1000` milliseconds runs after about one second and prints `2`.
