# Emacs Golf #056 — The Universal Fix
**Category:** G. Elisp and automation

Welcome to **Emacs Golf** — fewest keystrokes wins.

## The challenge
Starting buffer:

```
Hello ,world
emacs   rocks
time to go
```

Point: beginning of buffer

Target buffer:

```
Hello, world
emacs rocks
time to go.
```

## Task
One custom command must fix all three formatting mistakes in a single invocation: the misplaced comma spacing, the run of spaces, and the missing final period.

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
