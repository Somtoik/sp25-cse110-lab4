1. Line 12 prints: `3`. Although `i` is declared in the `for` loop with `var` it's function-scoped, so it’s still accessible after the loop ends. Since the array has 3 items `i` increments to 3 before stopping.
2. Line 13 prints: `150`. Even though `discountedPrice` was declared inside the for loop with `var` it’s still accessible here because `var` is function-scoped.
3. Line 14 prints: `150`. `finalPrice` was declared outside the loop with `var`, so it keeps getting updated inside the loop. The final value it held was the last product price (300) with the 0.5 discount applied (150).
4. This function returns `[50, 100, 150]`. Each price is cut in half, rounded, and pushed into the array. No console.log calls are active, so it just returns the array.
5. Line 12 throws a ReferenceError. `i` was declared using `let` inside the for loop, so it's block-scoped and doesn't exist outside the loop.
6. Line 13 throws a ReferenceError. `discountedPrice` was declared inside the for loop block using `let`, so it isn’t accessible outside that loop.
7. Line 14 prints: `150`. `finalPrice` was declared outside the loop using `let`, so it’s still accessible after the loop ends and holds the last calculated value.
8. This function returns `[50, 100, 150]`. Every price is halved and rounded before being added to the array. Nothing weird happens because everything is declared with `let` inside the right scope.
9. Line 11 throws a ReferenceError. `i` is declared with `let` inside the for loop block, so it doesn’t exist outside that block.
10. Line 12 prints: `3`. `length` was declared as a `const` outside the loop, so it's still accessible here and never changes.
11. The function returns `[50, 100, 150]`. The loop runs 3 times, each time calculating the discounted price and pushing it into the array.
12. Answers Below:
    A.`student.name`
    B.`student["Grad Year"]`
    C.`student.greeting()`
    D.`student["Favorite Teacher"].name`
    E.`student.courseLoad[0]`
13. Answers:
    A.`'3' + 2` = `'32'` → Java turns the number into a string and concatenates
    B.`'3' - 2` = `1` → Java converts the string to a number and subtracts
    C.`3 + null` = `3` → `null` becomes 0.
    D. `'3' + null` = `'3null'` → `null` becomes the string `'null'`.
    E.`true + 3` = `4` → `true` becomes 1.
    F.`false + null` = `0` → `false` is 0 and `null` is also 0.
    G.`'3' + undefined` = `'3undefined'` → `undefined` becomes the string `'undefined'`.
    H.`'3' - undefined` = `NaN` → `'3'` turns into 3 but `undefined` can’t convert to a number.
14. A. `'2' > 1` = `true` → `'2'` becomes 2, and 2 > 1.
    B.`'2' < '12'` = `false` → string comparison → `'2'` comes after  `'1'` in `'12'`.
    C.`2 == '2'` = `true` → loose comparison allows coercion.
    D.`2 === '2'` = `false` → type matters .
    E.`true == 2` = `false` → `true` becomes 1, but 1 != 2.
    F.`true === Boolean(2)` = `true` → `Boolean(2)` is `true`, and both are strictly `true`.
15. `==` allows type coercion, so `2 == '2'` is true.
`===` requires both value and type to match, so `2 === '2'` is false.
17. The result is `[2, 4, 6]`. This is because the `modifyArray` function loops through `[1,2,3]` and applies `doSomething()` (2X the number). So we get: doSomething(1) = 2, doSomething(2) = 4, doSomething(3) = 6 which are pushed into `newArr`, and returned.
19. The output is: 1,4,3,2. This is due to the fact that, 1 and 4 run immediately. 3 is set with 0 delay but still runs after said sync code, and 2 is delayed by 1 second.

