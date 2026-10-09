# Emacs Golf #035 — The Recursive Rabbit Hole
**Category:** D. Emacs-specific power moves

Welcome to **Emacs Golf** — fewest keystrokes wins.

## The challenge
Starting buffer:

```
outer context
[[nested detail]]
back to normal
```

Point: line 1, column 1

Target buffer:

```
outer context
[[hidden detail]]
back to normal
```

## Task
Enter a temporary recursive edit, change `nested` to `hidden` while inside it, then return to the original editing context. You must NOT be in a recursive edit when you finish, and point must be back at line 1, column 1.

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
