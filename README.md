# CSS calc() Function Unexpected Behavior

This repository demonstrates a common yet uncommonly understood issue with CSS's `calc()` function:  Unexpected behavior when calculations result in invalid CSS values or inconsistent unit usage.  The `bug.css` file showcases the problematic code, while `bugSolution.css` offers a corrected approach.

**Problem:** The `calc()` function, while powerful, can lead to unexpected results if not handled carefully. The primary issues demonstrated involve:

1. **Invalid Values:** Attempting to calculate negative values for properties that don't accept negative values (e.g., `width`, `height`).
2. **Inconsistent Units:** Mixing units within a single `calc()` expression (e.g., pixels and percentages) without proper consideration can lead to errors.

**Solution:** The solution lies in carefully considering the possible outcomes of `calc()` expressions and ensuring that they always result in valid and consistent CSS values.  This often involves using `max()` and `min()` functions to constrain the result to an acceptable range and employing consistent units throughout the calculation.