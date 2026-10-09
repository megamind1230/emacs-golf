# Emacs Golf #057 — The One-Key Challenge
**Category:** G. Elisp and automation

Welcome to **Emacs Golf** — fewest keystrokes wins.

## The challenge
Starting buffer:

```
  beta  
alpha  
gamma
```

Point: beginning of buffer

Target buffer:

```
> alpha
> beta
> gamma
```

## Task
One invocation of a single custom command must trim every line, sort them, and prefix each with `> ` . Declare the command in Setup.

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
