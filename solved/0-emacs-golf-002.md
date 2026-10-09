# Emacs Golf #002 — Sentence Surgery
**Category:** A. Basic editing and navigation

Welcome to **Emacs Golf** — fewest keystrokes wins.

## The challenge
Starting buffer:

```
I really really like Emacs.
```

Point: beginning of line

Target buffer:

```
I really like Emacs.
```

## Task
Delete only the second `really`.

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

Solution: `v really RET e Ls`
Setup: meow-mode
Explanation: `v really RET e` select the 2nd really, `L` also select trailing space, `s` delete selection

Solution: `v really RET e sd`
Setup: meow-mode
Explanation: `v really RET e` select the 2nd really, `s` delete selection {only word}, `d` delete 1 more character {which is the space}
