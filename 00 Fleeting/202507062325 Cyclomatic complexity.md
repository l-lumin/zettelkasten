# Cyclomatic Complexity

Cyclomatic Complexity (CC) is a software metric used to measure the complexity of a program. It quantifies the number of linearly independent paths through a program's source code. CC can be calculated at the function, class or application level.

## Formula

For a single function, CC is calculated using the control flow graph with this formula:
$CC = E - N + 2$

Where:

- E = the number of edges in the control flow graph
- N = the number of nodes in the control flow graph

A simpler way to think about it is:
`CC = D + 1`
Where D is the number of decision points (e.g., `if`, `while`, `for`, `case`).

Example:

```py
def decision(c1: int, c2: int):
    if c1 < 100:
        return 0
    if c1 + c2 > 500:
        return 1
    return -1
```

This function contains:

- 2 decision points (`if` statements), each introducing a new possible path
- A default path (the final `return`)

$CC = 3 - 2 + 2 = 3$
