---
title: "8 Git aliases that make me more efficient"
description: "Use aliases to create shortcuts for your most-used or complex Git commands."
pubDate: "Jan 05 2025"
image: "/index.webp"
categories:
  - tech
tags:
  - Makrdown
badge: Pin
---
Use aliases to create shortcuts for your most-used or complex Git commands.
Defining Git aliases to serve as substitutes for commands provides two major benefits:

- It simplifies long commands that have many options, making them shorter and easier to remember.
- It shortens frequently used commands so that you can work more efficiently.

## How to define and use aliases
To define a Git alias, use the `git config` command with the alias and the command you want to substitute. For example, to create the alias `p` for `git push`:
```bash
git config --global alias.p 'push'
```
```bash
git p
```
You can use an alias by providing it as an argument to `git`, just like any other command:
To see all your aliases, list your configuration with `git config`:
```bash
git config --global -l
user.name=ricardo
user.email=ricardo@example.com
alias.p=push
```

You can also define aliases with your favorite shell, such as Bash or Zsh. However, defining aliases using Git offers several features that you don't get using the shell. First, it allows you to use aliases across different shells with no additional configuration. It also integrates with Git's autocorrect feature, so Git can suggest aliases as alternatives when you mistype a command. Finally, Git saves your aliases in the user configuration file, allowing you to transfer them to other machines by copying a single file.

Regardless of the method you use, defining aliases improves your overall experience with Git. For more information about defining Git aliases, take a look at the [Git Book](https://git-scm.com/book/en/v2/Git-Basics-Git-Aliases).
## 8 useful Git aliases
Now that you know how to create and use an alias, take a look at some useful ones.
### 1. Git status
Git command line users often use the `status` command to see changed or untracked files. By default, this command provides verbose output with many lines, which you may not want or need. You can use a single alias to address both of these components: Define the alias `st` to shorten the command with the option `-sb` to output a less verbose status with branch information:
```bash
git config --global alias.st 'status -sb'
```
If you use this alias on a clean branch, your output looks like this:
```bash
git st
## master
```
Using it on a branch with changed and untracked files produces this output:
```bash
git st
## master
 M test2
?? test3
```

```bash
git config --global alias.ll 'log --oneline'
```
```bash
git config --global alias.last 'log -1 HEAD --stat'
```
```bash
git config --global alias.cm 'commit -m'
```
```bash
git config --global alias.rv 'remote -v'
```
```bash
git config --global alias.d 'diff'
```
```bash
git config --global alias.dv 'difftool -t vimdiff -y'
```
```bash
git config --global alias.gl 'config --global -l'
```
```bash
git config --global alias.se '!git rev-list --all | xargs git grep -F'
```

sourcelink: https://opensource.com/article/20/11/git-aliases