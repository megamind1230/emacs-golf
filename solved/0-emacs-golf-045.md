# Emacs Golf #045 — Window Tetris
**Category:** F. Buffers, windows, and navigation

Welcome to **Emacs Golf** — fewest keystrokes wins.

## The challenge
Starting buffer:

```
One window showing buffer alpha. Buffer beta also exists (hidden).
```

Goal:

```
Two side-by-side windows: left shows alpha, right shows beta.
```

## Task
Create the two-column layout. (First make sure you have 2 buffers {in memory/open})

## Rules
- Everything is allowed: vanilla Emacs, Evil, Meow, packages, macros, Elisp, custom keybindings, external tools.
- The result must match the target exactly. Correctness beats brevity.
- One key event per stroke: a chord such as `C-a` counts as one stroke.
- Disclose any setup, packages, macros, or custom commands your solution requires.

## How to submit
```
Solution:
Setup:
Explanation:
```

**The goal isn't to prove one editing style is superior. It's to discover how many different ways Emacs can solve the same problem.**

May the shortest sequence win.

## Solutions

Solution:
```
 C-x 3                  ;; split-window-right
 C-x o                  ;; other-window
 C-x b                  ;; switch-to-buffer
 s                      ;; self-insert-command
 c                      ;; self-insert-command
 RET
```
Setup: vanilla
Explanation: alpha is `emacs-golf-045.md`, beta is `*scratch*`
