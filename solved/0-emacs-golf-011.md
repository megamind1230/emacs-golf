# Emacs Golf #011 — Number Cruncher
**Category:** B. Multi-line transformations

Welcome to **Emacs Golf** — fewest keystrokes wins.

## The challenge
Starting buffer:

```
sun
moon
star
sky
sea
tree
rock
wind
fire
sand
```

Point: beginning of line 1

Target buffer:

```
1. sun
2. moon
3. star
4. sky
5. sea
6. tree
7. rock
8. wind
9. fire
10. sand
```

## Task
Prefix the ten lines with `1.` through `10.` .

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

Solution: `M-h C-x C-x C-b C-u C-x r N 1 RET %1d. SPC RET`
Setup: vanilla
Explanation: `M-h C-x C-x C-b` only select the desired region, the rest is just adjusting `rectangle-number-lines` arguments

Solution: `M-h ; H C-u C-x r N 1 RET %1d. SPC RET`
Setup: vanilla + meow-mode
Explanation: `M-h C-x C-x C-b` only select the desired region, the rest is just adjusting `rectangle-number-lines` arguments

Solution: `C-x C-w a.org RET M-h C-M-% ^ RET - SPC RET ! S-<right> S-<right>`
Setup: vanilla
Explanation: create an org file, replace start of lines with `- ` then change list style

Solution: `C-x C-k C-c 1 RET F3 F3 . SPC C-n C-a F4 M-9 F4`
Setup: vanilla
Explanation: `C-x C-k C-c 1 RET` makes sure that kmacro counter is set to 1, `F3 F3 . SPC` places the first `1. `, `C-n C-a` start of next line, `F4` end macro, `M-9 F4` repeat macro 9 times.
