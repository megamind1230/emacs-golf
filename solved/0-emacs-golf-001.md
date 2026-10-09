# Emacs Golf #001 — The Word Assassin
**Category:** A. Basic editing and navigation

Welcome to **Emacs Golf** — fewest keystrokes wins.

## The challenge
Starting buffer:

```
The quick brown fox jumps over the lazy dog.
```

Point: beginning of line

Target buffer:

```
The quick fox jumps over the lazy dog.
```

## Task
Delete `brown` plus its trailing space. Nothing else changes.

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

Solution: `eeeLs`
Setup: vanilla,  meow mode
Explanation: move to select the word `brown` then select the trailing space with `L` then `s` to delete selection

Solution: `M-f M-f M-d`
Setup: vanilla, cursor at the beginning of the line
Explanation: move forward 2 words, then delete 1 word
