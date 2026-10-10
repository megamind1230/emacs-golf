# Emacs Golf #021 — The Regex Monster
**Category:** C. Search and replace

Welcome to **Emacs Golf** — fewest keystrokes wins.

## The challenge
Starting buffer:

```
one    two
three     four  five
six
```

Point: beginning of line 1

Target buffer:

```
one two
three four  five
six
```

## Task
Replace every sequence of three or more spaces with exactly one space. Two-space runs must survive.

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

Solution: `M-x replace-regex SPC+ RET SPC`
Setup: vanilla
Explanation: `SPC+` for one or more spaces
