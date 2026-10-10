# Emacs Golf #012 — Prefix Parade
**Category:** B. Multi-line transformations

Welcome to **Emacs Golf** — fewest keystrokes wins.

## The challenge
Starting buffer:

```
write the report
review the patches
merge the branch
cut the release
```

Point: beginning of line 1

Target buffer:

```
TODO: write the report
TODO: review the patches
TODO: merge the branch
TODO: cut the release
```

## Task
prefix every line with `TODO:`

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

Solution: `M-h ; H M-x replace-regex RET ^ RET TODO: SPC`
Setup: vanilla + meow-mode
Explanation: `M-h ;` select paragraph then reverse the cursor to the other bound, `H` step back 1 char {now cursor is at the end of line 4} , do a regular expression replace
