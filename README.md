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
```

### STDIN

```
$ logit
```



