# Emacs Golf #082 — Occur Quest
**Category:** D. Emacs-specific power moves

Welcome to **Emacs Golf** — fewest keystrokes wins.

## The challenge
Starting buffer:

```
INFO boot
ERROR disk full
INFO cache
ERROR timeout
INFO ready
```

Point: beginning of buffer

Goal:

```
A separate *Occur* buffer exists, listing every line containing ERROR with its line number, and the source buffer is unchanged.
```

## Task
Collect all `ERROR` lines into their own view.

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
