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
