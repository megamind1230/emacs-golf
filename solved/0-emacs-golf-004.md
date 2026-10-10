# Emacs Golf #004 — Punctuation Surgery
**Category:** A. Basic editing and navigation

Welcome to **Emacs Golf** — fewest keystrokes wins.

## The challenge
Starting buffer:

```
Hello ,world !
```

Point: beginning of line

Target buffer:

```
Hello, world!
```

## Task
Fix the misplaced spaces around `,` and `!` without retyping the line.

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

Solution: `M-f C-f C-t M-f C-f C-t`
Setup: vanilla
Explanation: just moving and transposing

Solution: `F3 M-f C-f C-t F4 C-x e`
Setup: vanilla
Explanation: simple macro

solution: `F3 M-f C-f C-t F4 F4` (6 inputs)
setup: vanilla
explanation: `F4` runs the defined macro, no need to `C-x e`

Solution: `M-f C-d C-f SPC C-e C-b C-b C-d`
Setup: vanilla
Explanation: delete and write spaces

Solution: `M-f C-d C-f SPC C-e C-b C-b C-d`
Setup: vanilla
Explanation: delete and write spaces

Solution: `t, C-t wd`
Setup: meow-mode
Explanation: Til comma, transpose, end of word, delete
