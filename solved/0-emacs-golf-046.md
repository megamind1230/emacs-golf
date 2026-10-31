# Emacs Golf #046 — Buffer Rotate
**Category:** F. Buffers, windows, and navigation

Welcome to **Emacs Golf** — fewest keystrokes wins.

## the challenge
starting buffer:

```
you are opening `emacs-golf-046.md` on the left, `*scratch*` buffer on the right

cursor on left split
```

goal:

```
swap the windows {rotate them}

cursor still on `emacs-golf-046.md`
```

## task
switch to the named buffer in the fewest keystrokes.

## rules
- everything is allowed: vanilla emacs, evil, meow, packages, macros, elisp, custom keybindings, external tools.
- the result must match the target exactly. correctness beats brevity.
- one key event per stroke: a chord such as `c-a` counts as one stroke.
- disclose any setup, packages, macros, or custom commands your solution requires.
- count execution keystrokes, not the time you spent configuring emacs.

## how to submit
```
solution:
setup:
explanation:
```


**the goal isn't to prove one editing style is superior. it's to discover how many different ways emacs can solve the same problem.**

may the shortest sequence win.


## solutions

solution: `c-x wr right right`
Setup: vanilla + `repeat-mode` on
Explanation:
