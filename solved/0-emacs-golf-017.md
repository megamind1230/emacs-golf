# Emacs Golf #017 — Case Closed
**Category:** B. Multi-line transformations

Welcome to **Emacs Golf** — fewest keystrokes wins.

## The challenge
Starting buffer:

```
emacs is great
we love emacs
emacs rocks
```

Point: beginning of line 1

Target buffer:

```
Emacs is great
we love Emacs
Emacs rocks
```

## Task
Convert every occurrence of `emacs` to `Emacs`.

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

Solution: `M-% emacs RET Emacs RET !`
Setup: vanilla
Explanation: query-replace emacs into Emacs, `!` don't prompt/ask more questions
