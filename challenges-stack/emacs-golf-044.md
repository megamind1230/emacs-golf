# Emacs Golf #044 — The One-Liner
**Category:** E. Programming challenges

Welcome to **Emacs Golf** — fewest keystrokes wins.

## The challenge
Starting buffer:

```
(defun double (x)
  "Double X."
  (* x 2))
```

Point: beginning of buffer · Mode: emacs-lisp-mode

Target buffer:

```
(defun double (x) "Double X." (* x 2))
```

## Task
Collapse the function onto a single line. The code itself must not change.

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
