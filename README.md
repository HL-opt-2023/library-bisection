# Library Bisection Game

An interactive teaching activity about efficient search and the bisection principle. Identify the one library-owned book in a stack of 100 books using as few group tests as possible. The original game is preserved unchanged; the companion page provides instructions and teaching notes.

## Scenario

You have a stack of 100 books, and exactly one belongs to the library. An alarm system at the library exit is triggered whenever the books you carry through include that library book. If the selected books do not include it, the alarm stays silent. Your task is to identify the library book using as few trips through the alarm system as possible.

In the game, each test represents taking the selected books through the exit: **red means the alarm is triggered**, and **green means no alarm**.

## Open the game

**[Play the game in your browser](https://hl-opt-2023.github.io/library-bisection/)** — no sign-in or installation is required. The companion page reuses the original game and adds instructions and teaching notes.

For offline use, download [library-bisection.html](library-bisection.html) and open the downloaded file in a web browser. GitHub’s file view displays the HTML source; download it to play.

## How to play

1. Select a group of books by clicking individual books or dragging a selection rectangle. Shift-drag adds to a selection.
2. Test the selected group. **Red** means the library-owned book is in the group. **Green** means it is not.
3. Use the result to narrow the candidates, then select and test another group.
4. Test the target book by itself to finish.

Green tests fade the tested books. Red tests do not automatically fade books outside the selection, so keep track of what you have inferred. The “Still possible” count reflects green-test eliminations and may be larger than the number of candidates your reasoning leaves.

Use **Undo test** to reverse a test, **Restart** to try again with the same target, **Default** to reset with a different target, and **Hold to reveal** to check the hidden book.

## Teaching use

Ask learners to design a procedure that reduces the number of trials before introducing a standard algorithm. Have teams compare or compete using their own procedures, then discuss why balanced groups provide useful information regardless of the result. This combines active learning with a visual game and a short team challenge.

## Connection to bisection

Each trip through the library exit answers a yes/no question: “Does this group contain library property?” Carry roughly half of the remaining candidate books through the alarm system. If the alarm is triggered (red), the library book is in that half. If there is no alarm (green), it is in the half left behind. Repeat with roughly half of the remaining candidates until only one book remains. This repeated halving is the bisection strategy.

With 100 books, the largest remaining candidate set can shrink as follows:

**100 → 50 → 25 → 13 → 7 → 4 → 2 → 1**

Seven well-chosen tests are enough to identify the target by inference in the worst case, since 2⁶ < 100 ≤ 2⁷. If the last result leaves an untested singleton, the game's completion rule requires one additional test of that book to obtain a red result.

This is the same halving principle used in binary search and the numerical bisection method. Binary search halves an ordered search range; numerical bisection halves an interval containing a root. Here, the test halves a set of candidate books, and no ordering of the books is needed.

The worst-case bound assumes exactly one target, accurate alarm signals, and equal cost for each group test. Numerical bisection requires its own assumptions, such as continuity and an interval whose endpoints bracket a root; the book game illustrates the halving principle rather than those analytic conditions.

## Acknowledgment

This game and its accompanying documentation were prepared with help from OpenAI Codex. The original supplied HTML game is preserved unchanged in this repository.
