# Part 1 Answers

1. Line 9 prints `values added: 20`. Since `var` has function scope, `result` can be used inside the function, and the value becomes `10 + 10`.

2. Line 13 prints `final result: 20`. Because `var` is function-scoped, `result` is still accessible outside the `if` block but inside the same function.

3. We should avoid using `var` because it has function scope instead of block scope. This can make variables accessible in places we may not expect, which can cause naming conflicts and bugs. It is usually better to use `let` or `const`.

4. Line 9 prints `values added: 20`. The variable `result` is declared with `let` inside the `if` block, and line 9 is also inside that same block, so it can access `result`.

5. Line 13 returns an error. Since `let` has block scope, `result` only exists inside the `if` block. Line 13 is outside that block, so `result` is not defined there.

6. Line 9 does not print anything because the code returns an error before reaching line 9. The variable `result` is declared with `const`, so it cannot be reassigned on line 7.

7. Line 13 does not print anything because the code already returned an error on line 7. The error happens because a `const` variable cannot be reassigned after it is first assigned.
