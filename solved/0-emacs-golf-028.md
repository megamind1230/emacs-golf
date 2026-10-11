# Emacs Golf #028 — Rectangle Wizard
**Category:** D. Emacs-specific power moves

Welcome to **Emacs Golf** — fewest keystrokes wins.

## The challenge
Starting buffer:

```
The quick brown fox
jumps over the lazy
dog every day.
```

Point: beginning of line 1

Target buffer:

```
The q     brown fox
jumps     r the lazy
dog e     day.
```

## Task
Blank out the rectangular block covering columns 6-10 of all three lines with spaces. Everything outside the rectangle must survive.

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

Solution: `fu C-v e jj r SPC`
Setup: evil-mode
Explanation: simple visual block mode motions

Solution: `M-: (while (not (eobp)) (setq beg (progn (move-to-column (1- 6)) (point)) end (progn (move-to-column (1- 10)) (point))) (save-restriction (narrow-to-region beg end) (replace-region-contents beg end (make-string (length (buffer-substring-no-properties beg end)) ? ))) (beginning-of-line 2)) RET`
Setup: vanilla
Explanation: elisp code to mark in between the columns needed then replace the region with spaces

Solution: `C-: ua C-x SPC M-f C-n C-n C-x r c`
Setup: `avy-goto-char` + vanilla
Explanation: `C-: ua` go to the `u` in quick, `C-x SPC` rectangle-mark-mode, `M-f C-n C-n` select the rectangle region, `C-x r c` clears rectangle.
