# Emacs Golf #041 — Comment Commander
**Category:** E. Programming challenges

Welcome to **Emacs Golf** — fewest keystrokes wins.

## The challenge
Starting buffer:

```
(defun greet (name)
  (message "Hello, %s!" name))

;; (defun farewell (name)
;;   (message "Goodbye, %s!" name))
```

Point: line 1

Target buffer:

```
;; (defun greet (name)
;;   (message "Hello, %s!" name))

(defun farewell (name)
  (message "Goodbye, %s!" name))
```

## Task
swap the comments state of the these functions, make sure to have `emacs-lisp-mode` on.

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

Solution: `]d M-x comment-region RET ]d M-x uncomment-region RET`
Setup: vanilla + meow-mode
Explanation:
