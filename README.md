# Library Bisection Game

An interactive activity for the ATOR course -- Lecture 4: identify one missing library property. This repository preserves the original game for later reference.

## Open the game

Download [library-bisection.html](library-bisection.html), then open the downloaded file in a web browser. GitHub displays the HTML source; download it to play.

## How to play

1. Select a group of books by clicking individual books or dragging a selection rectangle. Shift-drag adds to a selection.
2. Test the selected group. **Red** means the target book is in the group. **Green** means it is not.
3. Use the result to narrow the candidates, then select and test another group.
4. Test the target book by itself to finish.

Green tests fade the tested books. Red tests do not automatically fade books outside the selection, so keep track of what you have inferred. The “Still possible” count reflects green-test eliminations and may be larger than the number of candidates your reasoning leaves.

Use **Undo test** to reverse a test, **Restart** to try again with the same target, **Default** to reset with a different target, and **Hold to reveal** to check the hidden book.

## Connection to bisection

Each test answers a yes/no question: “Is the target in this group?” To make each answer useful, select roughly half of the remaining candidates. A red result keeps the selected half; a green result keeps the other half. Repeat this process until only one candidate remains.

With 100 books, the largest remaining candidate set can shrink as follows:

**100 → 50 → 25 → 13 → 7 → 4 → 2 → 1**

Seven well-chosen tests are enough to identify the target by inference in the worst case, since 2⁶ < 100 ≤ 2⁷. If the last result leaves an untested singleton, the game's completion rule requires one additional test of that book to obtain a red result.

This is the same halving principle used in binary search and the numerical bisection method. Binary search halves an ordered search range; numerical bisection halves an interval containing a root. Here, the test halves a set of candidate books, and no ordering of the books is needed.

## Acknowledgment

This game and its accompanying documentation were prepared with help from OpenAI Codex. The original supplied HTML game is preserved unchanged in this repository.
