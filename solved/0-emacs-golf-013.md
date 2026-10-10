# Emacs Golf #013 — Suffix Parade
**Category:** B. Multi-line transformations

Welcome to **Emacs Golf** — fewest keystrokes wins.

## The challenge
Starting buffer:

```
let x = 1
let y = 2
return x + y
```

Point: beginning of line 1

Target buffer:

```
let x = 1;
let y = 2;
return x + y;
```

## Task
Append `;` to every line.

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

Solution: `M-h ; H M-x replace-regex RET $ RET ;`
Setup: vanilla + meow-mode
Explanation:
