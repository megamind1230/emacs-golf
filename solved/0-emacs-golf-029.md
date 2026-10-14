# Emacs Golf #029 — Register Roulette
**Category:** D. Emacs-specific power moves

Welcome to **Emacs Golf** — fewest keystrokes wins.

## The challenge
Starting buffer:

```
SNIPPET
==
^^
==
^^
==
^^
```

Point: beginning of line 1

Target buffer:

```
SNIPPET
==
SNIPPET
==
SNIPPET
==
SNIPPET
```

## Task
Copy the line `SNIPPET` into a register once, then replace each `^^` with the register's contents at all three positions.

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

Solution:`x C-x rsq C-M-% \^\^ RET C-x r i q RET !`
Setup: meow-mode + vanilla
Explanation:`x` select first line, `C-x rsq` copy to q register, regex replace `^^` with `insert whatever in register q`, `!` ask nothing

Solution:`x C-x rsq M-% ^^ RET C-x riq RET !`
Setup: meow-mode + vanilla
Explanation: no need for regex replace

Solution: `M-@ M-w C-M-% \^\^ RET C-y RET !`
Setup: vanilla
Explanation:

Solution: `M-@ M-w M-% ^^ RET C-y RET !`
Setup: vanilla
Explanation:

Solution: `yy:%s/\^\^/C-r"/g RET`
Setup: evil-mode
Explanation: maybe you can use `C-r +` too

Solution:
```
M-% ^^ RET ; query-replace ^^
C-t o      ; yank-thing-to-minibuffer, word. yanks the thing at point in
           ; minibuffer-selected-window into the minibuffer
RET a      ; perform replacement
```
Setup: conn.el
Explanation:

Solution:
```
C-SPC                  ;; set-mark-command
 C-e                    ;; move-end-of-line
 M-w                    ;; kill-ring-save
 C-n                    ;; next-line
 C-n                    ;; next-line
 C-c C->                ;; mc/mark-all-dwim
 C-y                    ;; yank
```
Setup: vanilla + multi-cursors.el
Explanation:
