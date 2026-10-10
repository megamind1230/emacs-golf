# Emacs Golf #016 — The Duplicate Purge
**Category:** B. Multi-line transformations

Welcome to **Emacs Golf** — fewest keystrokes wins.

## The challenge
Starting buffer:

```
apple
banana
apple
cherry
banana
date
cherry
```

Point: beginning of line 1

Target buffer:

```
apple
banana
cherry
date
```

## Task
Remove duplicate lines, preserving the first occurrence of each.

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

Solution: `M-h M-x delete-duplicate-lines`
Setup: vanilla
Explanation:
