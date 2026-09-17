# UNIX & Shell Programming — course repo

Coursework repo for **UNIX Shell Programming**, 3rd semester.
Full syllabus: `syllabus/unix-shell-programming.md` — read it before generating any lab work.

## Course facts

| | |
|---|---|
| Course | UNIX Shell Programming |
| Code | `CSAEC310` as printed in the syllabus; repo is named `24CSAEC39`; owner also refers to it as `24CS31`. Treat these as the same course. |
| Credits | 1:0:0 |
| Contact hours | 15L (lecture only — the lab work is the practical component per unit) |
| Pre-requisite | C Programming |
| Coordinators | Dr. Chandrika Prasad / Mamatha A |

## Unit map

Each unit has a lecture topic list and a lab component. Lab work is what lands in this repo.

**Unit I — Introduction to UNIX.** Architecture of UNIX, features of UNIX, the UNIX file system, the
`vi` editor, file handling utilities, security by file permissions.
Command inventory (the exam draws from exactly this list):
`PATH` `man` `echo` `printf` `script` `passwd` `uname` `who` `date` `stty` `pwd` `cd` `mkdir`
`rmdir` `ls` `cp` `mv` `rm` `cat` `more` `wc` `lp` `od` `tar` `gzip`
*Lab: basic Linux commands executed on the terminal.*

**Unit II — Introduction to Shells.** UNIX session; UNIX utilities; process utilities; disk utilities;
networking commands; text processing utilities; backup utilities.
*Lab: process / disk / text-processing commands on the terminal.*

**Unit III — Standard Streams.** Redirection, pipes, the `tee` command, command execution, quotes,
command substitution, aliases, variables, environment variables.
*Lab: customising the shell environment and redirection commands.*

**Unit IV — Filters.** Filters and pipes, concatenating files, displaying the beginning and end of
files, cut and paste, sorting, translating characters, files with duplicate lines, regular
expressions using `grep`.
*Lab: filter commands on the terminal.*

**Unit V — Shell Scripts.** `read` / making scripts interactive; command line arguments; `exit` and
exit status; logical operators `&&` and `||`; conditional execution; the `if` conditional; `test` and
`[ ]` to evaluate expressions; the `case` conditional; `expr` for computation and string handling;
`$0` / calling a script by different names; `while` looping; `for` looping with a list; `set` and
`shift` to manipulate positional parameters.
*Lab: shell script programs.*

## Scope discipline

This is a **first-course syllabus**. When writing scripts, stay inside the constructs the syllabus
names — a solution that reaches past them is wrong for this course even if it runs.

- Use `expr` for arithmetic, not `$(( ))`, unless asked otherwise. `expr` is the named construct.
- Use `test` / `[ ]`, not `[[ ]]`. `[[ ]]` is a bash extension the syllabus never introduces.
- Use `case` and `if`/`elif`/`else`/`fi` as written in Unit V.
- Prefer POSIX `sh` constructs. No arrays, no `local`, no process substitution, no `function` keyword.
- Backtick vs `$( )` command substitution: `$( )` is fine and clearer; mention backticks where the
  course notes use them.
- Keep to the Unit I command inventory for Unit I work; don't substitute a modern equivalent
  (`more`, not `less`; `od`, not `hexdump`).

## Script conventions

- `#!/bin/sh` shebang, or `#!/bin/bash` only when a bash-specific feature is genuinely required.
- Header comment on every script: program number, one-line statement of the problem.
- Mark scripts executable (`chmod +x`) and commit them that way.
- Include a **sample run** — the commands typed and the exact output — as a trailing comment block or
  a companion `.txt`. Lab records need the output transcript, not just the code.
- Comment for a student reader: explain the construct being demonstrated, since the point of each
  program is the construct.

## Repo layout

```
syllabus/     the course syllabus, verbatim
unit-01/ … unit-05/   lab work per unit (created as work is added)
```

## Git

- Commits are authored as the repo owner: `JNANOTTAM GY <jnanbelliappa135@gmail.com>`.
- Do **not** append `Co-Authored-By: Claude` or `Claude-Session:` trailers to commits in this repo.
