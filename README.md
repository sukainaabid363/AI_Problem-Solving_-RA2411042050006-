Course:** Artificial Intelligence
**Repository:** AI_ProblemSolving_-RA2411042050006
Problem 6 — Sudoku Solver (CSP)
### Problem Description
Sudoku is a logic-based number placement puzzle played on a 9×9 grid. Some cells are pre-filled, and the objective is to fill the remaining cells so that every row, column, and 3×3 subgrid contains the digits 1–9 without repetition.

The user can solve the puzzle manually through an interactive interface, or let the AI solve it automatically using a CSP backtracking algorithm.
### Algorithm Used — Constraint Satisfaction Problem (CSP) with Backtracking

The Sudoku puzzle is modeled as a CSP where:
- **Variables** — each empty cell in the 9×9 grid
- **Domain** — digits 1 to 9 for each cell
- **Constraints:**
  - Each row must contain digits 1–9 without repetition
  - Each column must contain digits 1–9 without repetition
  - Each 3×3 subgrid must contain digits 1–9 without repetition

**How the algorithm works:**
1. Find the next empty cell
2. Try placing digits 1–9 one by one
3. Check if the digit satisfies all three constraints
4. If valid → move to the next empty cell
5. If no digit works → backtrack to the previous cell and try the next digit
6. Repeat until all cells are filled

### Features
- 3 pre-loaded easy puzzles to choose from
- Auto Solve using CSP backtracking
- Hint button — reveals one correct random cell
- Manual play — click a cell and type a number or use the on-screen numpad
- Keyboard support — arrow keys to navigate, 1–9 to enter, Backspace to erase
- Conflict highlighting — invalid cells turn red automatically
- Win screen when puzzle is solved correctly

### How to Run
1. Download `sudoku_solver.html`
2. Open it in any modern web browser (Chrome, Firefox, Edge)
3. No installation or dependencies required — runs entirely in the browser

 ### Sample Output

**Input:** 9×9 grid with some pre-filled numbers (Easy Puzzle 1)
```
5 3 _ | _ 7 _ | _ _ _
6 _ _ | 1 9 5 | _ _ _
_ 9 8 | _ _ _ | _ 6 _
------+-------+------
8 _ _ | _ 6 _ | _ _ 3
4 _ _ | 8 _ 3 | _ _ 1
7 _ _ | _ 2 _ | _ _ 6
------+-------+------
_ 6 _ | _ _ _ | 2 8 _
_ _ _ | 4 1 9 | _ _ 5
_ _ _ | _ 8 _ | _ 7 9
```

**Output:** Fully solved grid where every row, column, and 3×3 box contains 1–9
```
5 3 4 | 6 7 8 | 9 1 2
6 7 2 | 1 9 5 | 3 4 8
1 9 8 | 3 4 2 | 5 6 7
------+-------+------
8 5 9 | 7 6 1 | 4 2 3
4 2 6 | 8 5 3 | 7 9 1
7 1 3 | 9 2 4 | 8 5 6
------+-------+------
9 6 1 | 5 3 7 | 2 8 4
2 8 7 | 4 1 9 | 6 3 5
3 4 5 | 2 8 6 | 1 7 9
