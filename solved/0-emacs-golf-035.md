# Emacs Golf #035 — The Recursive Rabbit Hole
**Category:** D. Emacs-specific power moves

Welcome to **Emacs Golf** — fewest keystrokes wins.

## The challenge

Starting buffer:

```text
(defun greet (name)
  (message "Hello, %s!" name))

(defun farewell (name)
  (message "Goodbye, %s!" name))
```

Point: beginning of line 1.

## Target buffer

```text
(defun greet (name)
  (message "Hello, %s!" name))

(defun farewell (name)
  (message "Goodbye, %s!" name))

(defun welcome (name)
  (message "Welcome, %s!" name))
```

## Task

Duplicate the `farewell` function and append the copy to the end of the buffer, renaming it to `welcome` and changing `Goodbye` to `Welcome`.

Preserve the original function exactly.

## Rules

- Everything is allowed: vanilla Emacs, Evil, Meow, packages, macros, Elisp, custom keybindings, external tools.
- The result must match the target exactly.
- One key event per stroke: a chord such as `C-a` counts as one stroke.
- Disclose any setup, packages, macros, or custom commands your solution requires.
- Count execution keystrokes, not configuration time.

## How to submit

```text
Solution:
Setup:
Explanation:
```

The goal isn't to prove one editing style is superior. It's to discover how many different ways Emacs can solve the same problem.

May the shortest sequence win.

## Solutions

Solution: `M-} xxy C-j C-j p C-: ga M-d i Welcome`
Setup: meow-mode + vanilla + avy
Explanation: mode to next paragraph{function}, yank last function, add 2 newlines, paste, avy-goto-char `g` {start of word Goodbye}, delete word, insert Welcome
