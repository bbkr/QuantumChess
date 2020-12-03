# QuantumChess v1.0.0

## Why?

I love chess. But this game is getting worn out.

Tournaments become less fun to watch every year. All openings, all gambits are explored so deeply by computer analysis that high level players go "out of theory" on 15th move. Mostly we see them replaying boring computer lines over and over again. Memoization wins with imagination.

On medium and amateur level there is still a lot to explore. However some people do not like deep thinking required by chess. They are better at resolving wide complexity than deep complexity, meaning that they can spot and counter 5 threats now than one threat after 5 moves.

So I wanted to create something fresh. Brain melting. That will restore imagination and fun in chess. Enjoy!

## Rules

### Superposition

Every piece starts in superposition state marked as 🟊.

It means that piece is everything at the same time - ♚, ♛, ♜, ♝, ♞ and ♟︎. Which will be written as ♚|♛||♜|♝|♞|♟︎ in this document.

<img src="/positions/start.png" width="512">


### Movement

Piece in superposition can move as any piece it can collapse to. So ♝|♜ can move any number of squares along a rank or file or any number of squares diagonally.
Player can choose which movement method to use during his turn.



