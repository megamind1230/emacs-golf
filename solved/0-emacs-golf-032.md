# Emacs Golf #032 — Narrow Escape
**Category:** D. Emacs-specific power moves

Welcome to **Emacs Golf** — fewest keystrokes wins.

## The challenge
Starting buffer:

```
(defun add-one (n)
  (setq n (+ n 1))
  n)

(defun shout (s)
  (upcase s))
```

Point: beginning of buffer · Mode: emacs-lisp-mode

Target buffer:

```
(defun add-one (n)
  (setq n (+ n 1))
  n)

(defun shout (s)
  (upcase (string-trim s)))
```

## Task
Restrict editing to the `shout` function, change `(upcase s)` to `(upcase (string-trim s))`, then restore the full buffer. The buffer must NOT be narrowed when you finish.

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

Solution: `M-> C-x nd C-: sac(string-trim SPC s C-x nw M-<`
Setup: meow-mode + vanilla + avy
Explanation: just make sure you did `M-x emacs-lisp-mode` before you start
