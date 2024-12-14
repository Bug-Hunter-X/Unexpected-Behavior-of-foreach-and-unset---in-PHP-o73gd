# PHP foreach and unset() Bug

This repository demonstrates a subtle but common error in PHP related to the interaction of `foreach` loops and the `unset()` function.  When you modify the array being iterated over within a `foreach` loop, the loop's behavior is not always what you'd expect.

This specific issue involves removing elements from an array while iterating over it.  The `unset()` function removes the element from the array, however, the internal array pointer used by the `foreach` loop may not adjust correctly, leading to skipped elements or unexpected index values.

The `bug.php` file shows a simple example that illustrates this behavior, while `bugSolution.php` offers a solution.