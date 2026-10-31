# Emacs Golf #049 — The Detour

**Category:** F. Buffers, windows, and navigation

Welcome to **Emacs Golf** — fewest keystrokes wins.

## The challenge

Starting state:
- The frame has **three windows**:
  - **Top-left** displays `a.txt`, point at line 10, column 1.
  - **Top-right** displays `b.txt`, point at line 20, column 1.
  - **Bottom** (full width) displays `c.txt`, point at line 30, column 1.
- The **top-left** window is selected.
- Buffer `notes.org` is open, point at line 1, column 1, but is not displayed.

Goal:

- The final layout is **exactly the starting layout** — same three windows, same buffers, same point positions, top-left selected.
- **In between**, you must have displayed `notes.org` in a single **full-frame** window (the whole frame showing only `notes.org`), then returned to the original layout.

This models the everyday "I need to read my notes without destroying my carefully arranged code layout" workflow.

## Task
Save the layout, blow it away to read `notes.org` full-frame, restore the exact layout.

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


Solution: `C-x r w a C-x 1 C-x b n TAB RET C-x r j a`
Setup: vanilla
Explanation:
```
  C-x r w a       save the 3-window configuration to register a
  C-x 1           delete other windows — the remaining window now
                  fills the frame
  C-x b n TAB RET switch that window to notes.org
                  (now notes.org is the only thing on the frame)
  C-x r j a       jump to register a, restoring all three windows,
                  their buffers, and their point positions
```
