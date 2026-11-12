# Windowsill Cats

A cat logic puzzle in one HTML file. One cat per row, column and coloured patch, and cats never touch, not even at the corners. No ads, no network, plays offline.

Open `index.html` in a browser. Add `?test=1` to run the puzzle core tests (`&n=40` sets puzzles per size).

## Build 13
- Straight drags: a drag-to-mark stroke locks to the row or column it sets off along, so drifting sideways or overshooting the edge cannot mark the line next door (Settings switch, on by default; off gives free drawing)

## Build 12
- Drag to mark: slide a finger across the board to put an × on every empty square it crosses; start on an × to rub marks out. One Undo step per stroke, never places a cat (Settings switch, on by default)
- Finger taps are handled from pointer events, so the first tap after a drag is no longer swallowed by the browser

## Build 11
- Auto ×: placing a cat fills a faint × on every square it rules out (Settings switch, on by default)
- Daily board: on claude.ai, signed-in players post their first solve time of the day to a shared list under the Daily puzzle. Needs the `db` and `user` artifact capabilities; the card stays hidden anywhere else
- A board pays out once: Undo/Redo lock after a win, and Restart or a reload cannot re-earn the level, win or cat
- Out of hearts freezes the board immediately; two quick wrong taps no longer leave a stuck red ring
- Forgiving refill no longer counts as a clean run, and the timer keeps running after it
- Single-tap mode: a quick second tap now really places an ×, and tapping an × clears it for free
- Hints can use one-step look-ahead and no longer give a reason that is not true of the board on screen
- Import and Erase validate the save, re-sync every control and deal a fresh board
- Keyboard: Enter or Space toggles an ×, C or Shift+Enter places a cat
- Unlocked palettes are readable in both light and dark theme
- Daily has its own best time, broken streaks show as 0, and the Daily is filed under the date it was dealt

## Build 10
- Locked starter cats: Normal gives extra starters until the board is easy to open, Hard gives one, Expert gives none
- Difficulty picker (Normal / Hard / Expert) for Levels and Free play
- Out of hearts now loses the board (Try again or New board). "Forgiving hearts" in Settings brings back the free refill
- Hint points at the next square and explains why; tap again to place the cat
- Restart button: same board, fresh hearts and clock
- Optional bonus boards after every 4th level: one heart, no hints, rarer cat, never block level progress
