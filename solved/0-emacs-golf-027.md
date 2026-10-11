# Emacs Golf #027 — Macro Machine
**Category:** D. Emacs-specific power moves

Welcome to **Emacs Golf** — fewest keystrokes wins.

## The challenge
Starting buffer:

```
alice item01
bob item02
carol item03
dave item04
erin item05
frank item06
grace item07
heidi item08
ivan item09
judy item10
karl item11
laura item12
mike item13
nancy item14
oscar item15
peggy item16
quinn item17
ruth item18
stan item19
tina item20
```

Point: beginning of line 1

Target buffer:

```
item01 alice
item02 bob
item03 carol
item04 dave
item05 erin
item06 frank
item07 grace
item08 heidi
item09 ivan
item10 judy
item11 karl
item12 laura
item13 mike
item14 nancy
item15 oscar
item16 peggy
item17 quinn
item18 ruth
item19 stan
item20 tina
```

## Task
Swap the two words on each of the 20 lines. Your submission must declare the technique you used (macro, regexp, Elisp, ...).

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

Solution: `<f3> .e G ee a SPC ESC R j <f4> M-1 M-9 <f4>`
Setup: vanilla + meow-mode
Explanation: record a macro, `.e G` grab first column {word}, `ee a SPC ESC` move after 2nd and insert space, `R` swap grabbed region with this place, `j` next line, end macro, repeat 19 more times
