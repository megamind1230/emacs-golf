# Emacs Golf #020 — Word Boundaries
**Category:** C. Search and replace

Welcome to **Emacs Golf** — fewest keystrokes wins.

## The challenge
Starting buffer:

```
cat category catlike
the cat sat
concatenate
```

Point: beginning of line 1

Target buffer:

```
dog category catlike
the dog sat
concatenate
```

## Task
Replace `cat` with `dog`, but leave `category`, `catlike` and `concatenate` untouched.

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

Solution: `M-% cat SPC RET dog SPC RET !`
Setup: vanilla
Explanation: that's a workaround, not a real solution, cuz we didn't do anything related to bounds
