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

Solution: `:%s/\s\([,!]\)/\1 /g RET M-x whitespace-cleanup`
Setup: evil-mode
Explanation: Regex match spaces followed by either , or ! characters, replace those with the matched character followed by a space, then call whitespace-cleanup to get rid of the training end of line (I mean you could also do that with another regex but whatever, lets do weird stuff)

Solution: `wXp$X`
Setup: evil-mode
Explanation: Instead of using f SPC like others have done, use w and Xp transpose before cursor. Though, then have to use $ instead of ; to go to around !.

Solution: `f SPC x p ; x p`
Setup: evil-mode
Explanation:

Solution: `f SPC x p f SPC x`
Setup: evil-mode
Explanation:

Solution: `M-: (let ((re (re-search-forward (rx "Hello " (group ",") "world" (group " !")))) (target "Hello, world!")) (when re (goto-char (match-beginning 1)) (delete-char 1) (goto-char (1- (point))) (insert ?,) (goto-char (match-beginning 2)) (delete-char 1) (cl-assert (string= (buffer-substring-no-properties (point-min) (point-max)) target))))`
Setup: vanilla
Explanation: Using re-search-forward to find the comma and the exclamation, (assuming you are in a buffer with only that text (without a newline)), and changing the buffer content, cl-assert is only to ensure it didn't fail lol
