# Emacs Golf #053 — Self-Binding
**Category:** G. Elisp and automation

Welcome to **Emacs Golf** — fewest keystrokes wins.

## The challenge
Starting buffer:

```
one two three four
```

Point: beginning of line

Target buffer:

```
ONE TWO THREE four
```

## Task
Pick a key, bind a command of your choice to it, and use that binding to uppercase the next three words. The binding itself belongs in Setup; the three words must be changed through it.

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
