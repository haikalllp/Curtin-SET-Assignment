  ## Sudoku.java:

```java title:"isSafe()"
// A1 ▶ Entry
public static boolean isSafe(int[][] board, int row, int col, int num) {
    // A2: for (int d = 0; d < board.length; d++) {
    for (int d = 0; d < board.length; d++) {
        // A3: if (board[row][d] == num) return false;
        if (board[row][d] == num) {
            return false;          // A4 ▶ exit via row‐violation
        }
    }
    // A5: for (int r = 0; r < board.length; r++) {
    for (int r = 0; r < board.length; r++) {
        // A6: if (board[r][col] == num) return false;
        if (board[r][col] == num) {
            return false;          // A7 ▶ exit via col‐violation
        }
    }
    // A8: int sqrt = …; int boxRowStart = …; int boxColStart = …;
    int sqrt = (int) Math.sqrt(board.length);
    int boxRowStart = row - row % sqrt;
    int boxColStart = col - col % sqrt;
    // A9: for (int r = boxRowStart; r < boxRowStart + sqrt; r++) {
    for (int r = boxRowStart; r < boxRowStart + sqrt; r++) {
        // A10: for (int d = boxColStart; d < boxColStart + sqrt; d++) {
        for (int d = boxColStart; d < boxColStart + sqrt; d++) {
            // A11: if (board[r][d] == num) return false;
            if (board[r][d] == num) {
                return false;      // A12 ▶ exit via subgrid‐violation
            }
        }
    }
    // A13: return true;
    return true;                  // A14 ▶ normal exit
}
```

```java title:"solveSudoku()"
// B1 ▶ Entry
public static boolean solveSudoku(int[][] board, int n) {
    int row = -1, col = -1;
    boolean isEmpty = true;
    // B2: find next empty cell
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n; j++) {
            if (board[i][j] == 0) {
                row = i; col = j;
                isEmpty = false;
                break;          // B3 ▶ break inner
            }
        }
        if (!isEmpty) {      // B4 ▶ break outer
            break;
        }
    }
    // B5: if (isEmpty) return true;
    if (isEmpty) {
        return true;         // B6 ▶ exit via “solved”
    }
    // B7: for (num=1; num<=n; num++)
    for (int num = 1; num <= n; num++) {
        // B8: if (isSafe(...))
        if (isSafe(board, row, col, num)) {
            board[row][col] = num;             // B9
            if (solveSudoku(board, n)) {       // B10: recursive
                return true;                   // B11 ▶ exit via solved
            } else {
                board[row][col] = 0;           // B12 backtrack
            }
        }
        // B13 → next num
    }
    // B14: none worked → return false
    return false;                            // B15 ▶ exit via “unsolvable”
}

```
