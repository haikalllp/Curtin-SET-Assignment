---

excalidraw-plugin: parsed
tags: [excalidraw]

---
==⚠  Switch to EXCALIDRAW VIEW in the MORE OPTIONS menu of this document. ⚠== You can decompress Drawing data with the command palette: 'Decompress current Excalidraw file'. For more info check in plugin settings under 'Saving'


# Excalidraw Data

## Text Elements
isSafe(int[][] board, int row, int col, int num) ^468CU1XP

1 ^ruz208Lz

2 ^yVbs1Rbk

Parameters:

def(1) = {int[][] board, int row, int col, int num} ^fKhWFZsu

def(2) {d=0}
use(2) {d, board}
for (int d = 0; d < board.length; d++) ^2lvvngcl

3 ^sRuG7RMa

5 ^bHd76Amd

use(2,3) = {d < board.length} ^QlwPkSRB

use(2,5) = {d > board.length} ^1a5Xx58o

use(3) = {board}
if (board[row][d] == num) ^mm4j4sZz

use(3,4) = {board[row][d] == num} ^gsKZNRnR

use(3,2) = {board[row][d] != num}
use(3,2) = {d++} ^XqDF07nQ

def(5) = {int r = 0}
use(5) = {r, board.length)
for (int r = 0; r < board.length; r++) ^QNr218xw

6 ^uZQl11L5

use(5,6) = {r < board.length} ^wKmVkeEi

use(6) = {board}
if (board[r][col] == num) ^kkWsIHwl


use(6,7) = {board[r][col] == num} ^1OO3LwWe

use(6,5) = {board[r][col] != num}
use(6,5) = {r++} ^5a89FL3b

8 ^g06c5hsc

use(5,8) = {r > board.length} ^oDpbabMR

def(8) = {int sqrt = (int) Math.sqrt(board.length)}
def(8) = {int boxRowStart = row - row % sqrt}
def(8) = {int boxColStart = col - col % sqrt}

use(8) = {sqrt, row, col, board.length} ^lhFSRuSF

9 ^sbjVqHLs

def(9) = {int r = boxRowStart}
use(9) = {r, boxRowstart, sqrt}
for (int r = boxRowStart; r < boxRowStart + sqrt; r++) ^DBDflcss

10 ^ox1zmRuC

def(10) = {int d = boxColStart;}
use(10) = {d, boxColStart, sqrt}
for (int d = boxColStart; d < boxColStart + sqrt; d++) ^bYE2bOka

r < boxRowStart + sqrt ^AgkoyQXA

r > boxRowStart + sqrt ^FigaHoeo

use(10,11) = {d < boxColStart + sqrt} ^S35i4JNY

11 ^6HAoUZ2K


use(11) = {if (board[r][d] == num)} ^WSBJLkSC

use(11,10) = {board[r][d] != num} ^jxIfHUmY

use(11,12) = {board[r][d] == num} ^3bMRHI3w

use(10,9) = {d > boxColStart + sqrt}
use(10,9) = {r < boxRowStart + sqrt}
use(10,9) = {r++} ^lMW0p453

13 ^FaEZSSBU

return true; ^5Lg9gfxs

12 ^ym550K6G

return false; ^25vhDEPm

7 ^2omgX6i6

return false; ^j8AD8ZC3

4 ^epzVESdM

return false; ^YQBiac6U

14 ^1r4BXLfv

END ^WqtuBZZJ

Start ^zeB7izEc

%%
## Drawing
```compressed-json
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

eh8Ye39njE7gxycICPwH4CqCAA==
```
%%