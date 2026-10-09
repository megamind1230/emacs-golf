# Emacs Golf #041 — Comment Commander
**Category:** E. Programming challenges

Welcome to **Emacs Golf** — fewest keystrokes wins.

## The challenge
Starting buffer:

```
x = 1
y = 2
z = x + y
```

Point: line 1

Target buffer:

```
x = 1
y = 2
z = x + y
```

## Task
Comment out the three-line region, then uncomment it again. The final buffer equals the starting buffer - your submission must show both steps performed in order, and the score covers both.

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
