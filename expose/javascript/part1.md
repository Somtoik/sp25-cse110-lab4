1. Line 9 prints: `values added: 20'. The add arguement enters the if block and caluclates the result because it is true.
2. Line 13 prints: `final result: 20`. Although the result was declared inside the if block it still works because `var` is function-scoped (not block-scoped like let/const).
3. You shouldn’t use `var` because it ignores block scoping. That makes it super easy reuse variables in different parts of your code without noticing, making it harder to manage overall
4. Line 9 prints: `values added: 20`. The `let result = 0` is only accessible inside the if block and line 9 is still inside that block, so it works fine.
5. Line 13 causes a ReferenceError. That’s because `let` is block-scoped, and since `result` was declared inside the `if` block, it doesn’t exist outside of it.
6. Line 9 throws an error. `const result = 0` declares `result` as a constant and then on line 7 we try to change it with `result = num1 + num2` (not allowed for constants).
7. Line 13 would also throw a ReferenceError if it got there, but the code already breaks above at line 7, so line 13 never runs.
   