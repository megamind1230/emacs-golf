# Emacs Golf #023 — Case-Insensitive Assassin
**Category:** C. Search and replace

Welcome to **Emacs Golf** — fewest keystrokes wins.

## The challenge
Starting buffer:

```
I love emacs
Emacs is great
EMACS FOREVER
```

Point: beginning of line 1

Target buffer:

```
I love editor
editor is great
editor FOREVER
```

## Task
Replace `emacs`, `Emacs` and `EMACS`regardless of the case with `editor`.

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

Solution: `<f3> C-s e m M-b M-d e d i t o r <f4> M-2 <f4>`
Setup: vanilla
Explanation: Record macro of finding, deleting and retyping the first instance, then run the macro twice.


Solution: `C-M-% emacs RET editor RET`
Setup: vanilla
Explanation: just make sure at first to toggle off the case-replace into nil {so that when replacing, it wouldn't respect the case of the original text}, now search and replace, and you add this elisp code to your config to toggle the case-replace variable value on deman.
```elisp
;; toggle the case replace variable
(defun dt/toggle-case-replace ()
  "Toggle case preservation during query replacement."
  (interactive)
  (setq case-replace (not case-replace))
  (message "case-replace: %s" case-replace))
(global-set-key (kbd "C-c t c r") #'dt/toggle-case-replace)
```

Solution: `2w*cgneditor<Esc>..`
Setup: evil-mode with evil-search-module set to evil-search and evil-ex-search-case set to its default value of smart. Explanation: Executing `*` on the lowercase emacs string case-fold searches for all the strings to replace. After `cgn` to change the match it suffices to repeat it twice with `..`
