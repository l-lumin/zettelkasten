# Question for clear explanation

1. What is expected?
2. What is actually happening?
3. What is the reason (root cause)?
4. Why does the fix resolve it?

---

## Example

Bug: a counter shows 3 instead of 2

1. Expected
 - The counter should show 2 after clicking the button twice
2. Actual
 - The counter shows 3 after clicking the button twice
3. Root cause
 - The counter is increased in two places
  - once in `useEffect`
  - once in `onClick`
4. Why the fix works
 - Removed the extra increment in `useEffect`, so each click adds only 1
