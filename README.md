# logit

Log URLs and other snippets of text, using the git commit log.

The envisioned use case is for someone who takes paper notes and wants to refer
to a paste or URL. The first few characters of the commit ID can be used.

## Setup

```
mkdir ~/log
cd ~/log
git init
printf "*\n" > .gitignore
git remote add origin git@git.mygitserver.org:~me/log
printf "export LOGIT_DIR='~/log'\n" >> ~/.bashrc
```

## Usage

### One-liner

```
$ logit foo
[trunk abcdefg] foo
$
```

### STDIN

```
$ logit
Enter text, end with Ctrl-D.
Here's an example longer log entry.

This is a test.
^D
[trunk 1234567] Here's an example longer log entry.
$
```

### searching

```
$ findit 1234

commit 1234567890abcdef1234567890abcdef12345678
Author: J Doe <jdoe@example.com>
Date:   Mon Sep 1 10:00:00 2022 -0000

    Here's an example longer log entry.

    This is a test.
```

