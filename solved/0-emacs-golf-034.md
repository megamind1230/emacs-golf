# Emacs Golf #034 — The Undo Maze
**Category:** D. Emacs-specific power moves

Welcome to **Emacs Golf** — fewest keystrokes wins.

## The challenge
Starting buffer:

```
delta ALPHA gamma
```

Point: end of buffer

Target buffer:

```
alpha beta gamma
```

## Task
Three edits were applied to reach the starting buffer from `alpha beta gamma`: delete `beta `, insert `delta ` at the front, upcase `alpha`. Undo exactly those three edits and stop - undoing any earlier change is a foul.

## Rules
- Everything is allowed: vanilla Emacs, Evil, Meow, packages, macros, Elisp, custom keybindings, external tools.
- The result must match the target exactly. Correctness beats brevity.
- One key event per stroke: a chord such as `C-a` counts as one stroke.
- Disclose any setup, packages, macros, or custom commands your solution requires.
- Count execution keystrokes, not the time you spent configuring Emacs.

## How to submit
```
Solution:
Setup:
Explanation:
```


**The goal isn't to prove one editing style is superior. It's to discover how many different ways Emacs can solve the same problem.**

May the shortest sequence win.

## Solutions

Solution: `M-f M-d ma delta M-u M-3 C-/`
Setup: vanilla + meow-mode
Explanation: start with `alpha beta gamma`delete 2nd word {beta}, `ma delta` to add it to start of line, `M-u` to upcase-word {ALPHA}, undo 3 times
