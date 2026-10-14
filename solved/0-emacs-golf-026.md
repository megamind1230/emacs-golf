# Emacs Golf #026 — We Only Need The First
**Category:** C. Search and replace

Welcome to **Emacs Golf** — fewest keystrokes wins.

## The challenge
Starting buffer:

```
the the quick fox fox jumps
```

Point: beginning of line 1

Target buffer:

```
the quick fox jumps
```

## Task
Find the first word that occurs twice consecutively and delete its second occurrence.

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

Solution: `dwff.`
Setup: evil-mode
Explanation: With only two duplicates there is no need for anything fancy, {counts as a workaround, cuz we didn't delete the 2nd occurrences}

Solution: `eeLs tjbHs`
Setup: meow-mode
Explanation: workaround and bruteforce

Solution: `eeLs eeeLs`
Setup: meow-mode
Explanation: workaround and bruteforce


Solution:
```
M-%
\(\w+\) \1 RET
\1 RET
!
```
Setup: vanilla
Explanation: `\N` backrefs can be used in the search pattern, capture group replacing

Solution: `M-d C-d C-: SPC s M-d`
Setup: vanilla + `avy-goto-char` from `avy` package, bound to `C-:`
Explaination: simple avy jumps

Solution: `M-d C-d M-3 M-f M-d`
Setup: vanilla
Explanation: simple deletions, with a calculated jump

Solution: `M-f M-d M-f M-d`
Setup: vanilla
Explanation:

Solution: `M-: (let* ((content (buffer-substring-no-properties (point-min) (point-max))) (times 0)) (dolist (strings (split-string content " ")) (save-excursion (while (re-search-forward strings nil t) (setq times (1+ times)))) (if (= times 2) (delete-region (match-beginning 0) (1+ (match-end 0))) (setq times 0)))) RET`
Setup: vanilla
Explanation:

Solution: `e M-d e M-d`
Setup: meow-mode
Explanation:

Solution: `M-d d v f RET M-d`
Setup: meow-mode
Explanation:

Solution:
```
d f o     ; kill-thing, dispatch, word.
          ;   dispatch places labels at each thing, similar to avy.
          ;   when the label at a thing is selected the action is
          ;   performed on that thing.  in this case the action is
          ;   kill-thing and the thing is word.
<mouse-1> ; select word to kill by left clicking on the second "the".
          ;   labels may also be selected by clicking on the thing
          ;   they are labeling.
<mouse-3> ; repeat last dispatch at right click (on the second "fox")
```
Setup: using conn.el modal system [mtll/conn: Another modal keybinding mode for Emacs](https://github.com/mtll/conn)
Explanation:
