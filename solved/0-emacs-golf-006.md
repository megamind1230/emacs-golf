# Emacs Golf #006 — End of the World
**Category:** A. Basic editing and navigation

Welcome to **Emacs Golf** — fewest keystrokes wins.

## The challenge
Starting buffer:

```
line 01
line 02
line 03
line 04
line 05
line 06
line 07
line 08
line 09
line 10
```
Point: beginning of line 1

Goal:

```
Point sits at end of buffer (just after the final character of line 10). The buffer text is untouched.
```

## Task
Travel from the very top to the very bottom.

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

Solution: `M-> C-b`
Setup: vanilla
Explanation:

Solution: `M-} C-b`
Setup: vanilla
Explanation:

Solution: `M-h C-x C-x C-b C-g`
Setup: vanilla
Explanation:

Solution: `]bh`
Setup: meow-mode
Explanation: `]b` select till end of buffer, `h` move to left {which just deselects btw}
