# QuantumChess v1.0.0

## Why?

I love chess. But this game is getting worn out.

Tournaments become less fun to watch every year. All openings, all gambits are explored so deeply by computer analysis that high level players go "out of theory" on 15th move. Mostly we see them replaying boring computer lines over and over again. Memoization wins with imagination.

On medium and amateur level there is still a lot to explore. However some people do not like deep thinking required by chess. They are better at resolving wide complexity than deep complexity, meaning that they can spot and counter 5 threats now than one threat after 5 moves.

So I wanted to create something fresh, brain melting. With sneaky tactics, havoc and suicides. Enjoy!

## Rules

### Superposition

Every piece starts in superposition state marked as 🟊.

It means that piece is everything at the same time - ♚, ♛, ♜, ♝, ♞ and ♟︎.

Which will be written as ♚|♛||♜|♝|♞|♟︎ in this document.

<img src="/positions/rules-superposition-1.png" width="400">

Such piece in superposition state can finally become any of those specific pieces in a process named [collapsing](#collapsing).

Note that it does **not** mean that player has for example 16 ♛. There is still one ♚, one ♛, two ♜, two ♝, two ♞ and eight ♟︎ available for him. But it is unknown which one is which.

### Movement

Piece in superposition can move as any piece it can collapse to.

Player must choose which movement method to use during his/her turn, so here is how white can begin with *d2* piece, which is ♚|♛||♜|♝|♞|♟︎:

<img src="/positions/rules-movement-1.png" width="400">

For example player may choose to move this piece as a ♞ to *b3* or as a ♛ to *d6*.

Accordingly ♝|♜ piece can move any number of squares along a rank/file or any number of squares diagonally, but can not move like a ♞.

### Collapsing

Collapsing is a process of losing ability to become some specific piece until single option remains. This can happen during movement or captures.

The easiest collapse is this move:

<img src="/positions/rules-collapsing-1.png" width="400">

Piece could be ♚|♛||♜|♝|♞|♟︎ and player decided to move it as a ♞. That means it can no longer become ♚, ♛, ♜, ♝ or ♟︎ because there cannot be "a ♜ that was jumping like ♞ in the past".

Time for something more advanced:

<img src="/positions/rules-collapsing-2.png" width="400"><img src="/positions/rules-collapsing-3.png" width="400">

Here ♚|♛||♜|♝|♞|♟︎ moved to d6 and only ♛ or ♜ could do that. So this piece lost ability to collapse to ♚, ♝, ♞ or ♟︎ and became ♛|♜. Then it moved to *a3* and only ♛ could do that. So that piece lost ability to become ♜ and finally collapsed to only possible state - ♛.

More than one piece can collapse during turn:

<img src="/positions/rules-collapsing-4.png" width="400"><img src="/positions/rules-collapsing-5.png" width="400">

Here player made 3 moves (all shown at once, black moves are skipped to avoid complexity). Each moved piece collapsed to ♛|♝. Also because player can have only one ♛ and two ♝ it implies that other pieces collapsed to ♚||♜|♞|♟︎ - every moved pieces must became ♛ or ♝ so those possibilities are taken. Then after *b6* move this piece collapsed to final ♛. That takes away possibility of becoming ♛ for *d4* and *d5* pieces - they have no other option than to collapse to ♝.

