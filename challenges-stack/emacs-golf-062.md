# Emacs Golf #062 — Kill to the Horizon
**Category:** A. Basic editing and navigation

Welcome to **Emacs Golf** — fewest keystrokes wins.

## The challenge
Starting buffer:

```
First paragraph with several words here.

Second paragraph too.
```

Point: line 1, column 16 (on the space after `paragraph`)

Target buffer:

```
First paragraph

Second paragraph too.
```

## Task
Delete from point to the end of the paragraph in one motion.

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
