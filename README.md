# discord-chess
Play chess in 32 or less on Discord.

## Commands
### Game related
| command name | explanaition |
| :- | :- |
| `.` | renders the scene |
| `.join` or `.j` | will make you join the game |
| `.quit` or `.q` | will kick you out from the current game players |
| `.users` or `.u` | lists all the users that are currently playing |
| `.start` or `.s` | will create a chess board with as many pieces as current players |
| `.stop` | will clear the board and stop the current game |
| `.empty` | clears the board |
| `.help ita` | explains all the italian terms used |
| `.help debug` | shows debug commands |
| `.help <(italian) letter of a piece>` | to get info and rules about it |
| `.help <(english) piece name>` | same as above |
`<param>` means mandatory parameter; `[param]` means optional parameters

### Debug
Left them in, cuz why not? **WARN**: i might have disabled some of these
| command name | explanaition |
| :- | :- |
| `.set <X> <Y> [<type> <team>] | [empty]` | to create a piece on the board |
| `.set <X> <Y> empty` | to clear a tile on the board |
| `.index <piece index> <team>` | gets the tile position from index and team of standard chess |
| `.index all <team>` | lists all the indices of a team |
| `.iset <index> <team> [<type> <team>] | [empty]` | like `.set` but from `.index` | 
| `.umove <X> <Y> <to X> <to Y>` | to move piece without rules |
| `.reset` | sets the board to standard chess |
| `.ping` | pong! |
| `.emoji <emoji name>` | sends an emoji from the server from name |

<style> img { width:20px; } </style>

### Pieces
- ![](./img/wbp.png) **Pawn**: `p`\
The pawn's moving message sintax is `<direction>`.\
The direction can be `8` (up), `2` (down), `4`, `6`.\
`4` and `6` will both go rigth if the piece is black, left if the piece is white.\
The same horizontal direction is applied to `7`, `9`, `1` and `3`.
- ![](./img/wbt.png) **Rook**: `t`\
The rook's moving message sintax is `<direction>[how many times]`.\
The direction can be `8`, `2`, `4` and `6`.\
This move will be played the times that the second parameters says, a number from `0` to `9`.
- ![](./img/wbq.png) **Queen**: `q`\
The queen's moving message sintax is `<direction>[how many times]`.\
The direction can be every number from `1` to `9` except `5`.\
This move will be played the times that the second parameters says, a number from `0` to `9`.
- ![](./img/wbk.png) **King**: `k`\
The king's moving message sintax is `<direction>`.\
The direction can be `8`, `2`, `4` and `6`.\
- ![](./img/wba.png) **Bishop**: `a`\
The bishop's moving message sintax is `<direction>[how many times]`.\
The direction can be `7`, `9`, `1` and `3`. This move will be played the times that the second parameters says, a number from `0` to `9`.
- ![](./img/wbc.png) **Knight**: `c`\
The knight's moving message sintax is `<first direction><second direction>`.\
The first direction can be `8`, `2`, `4` and `6`.\
The second one needs to be one of the two diagonal keys next to it.\
eg:
    - `23` = L (2 down, 1 rigth);
    - `87` = ꓶ (2 up, 1 left);
    - `21` = ⅃ (2 down, 1 left);
    - `27` = invalid move.