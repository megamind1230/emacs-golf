# Emacs Golf #025 — Parenthesis Hunt
**Category:** C. Search and replace

Welcome to **Emacs Golf** — fewest keystrokes wins.

## The challenge
Starting buffer:

```
(defun square (x) (* x x))
```

Point: on the ` (` of `(* x x)` (column 19) · Mode: emacs-lisp-mode

Goal:

```
Point sits on the matching )  that closes that opening parenthesis. Buffer text untouched.
```

## Task
Jump to the matching closing parenthesis from the given opening one.

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

Solution: `C-M-f`
Setup:
Explanation: [GNU Emacs FAQ](https://www.gnu.org/software/emacs/manual/html_mono/efaq.html#How-do-I-show-which-parenthesis-matches-the-one-I_0027m-looking-at_003f)
