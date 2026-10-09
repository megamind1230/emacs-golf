# Emacs Golf #028 — Rectangle Wizard
**Category:** D. Emacs-specific power moves

Welcome to **Emacs Golf** — fewest keystrokes wins.

## The challenge
Starting buffer:

```
The quick brown fox
jumps over the lazy
dog every day.
```

Point: beginning of line 1

Target buffer:

```
The q     brown fox
jumps     the lazy
dog e     day.
```

## Task
Blank out the rectangular block covering columns 6-10 of all three lines with spaces. Everything outside the rectangle must survive.

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
