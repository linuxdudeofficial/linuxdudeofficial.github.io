---
title: How to create bash aliases (command shortcuts)
image:
  path: "/static/article-pics/bash-aliases.jpg"
  height: 800
  width: 480
layout: post
date: '2019-04-27 02:17:36'
author: thecodefreak
tags:
- bash
- bashalias
- linuxbash
- commandalias
comment: true
featured: true
category: Linux
---

Even if you were not aware of this aliases functionality you might have been thought about this.  Instead calling a commonly used long command line to single word? It's quite useful right? Yes it is :D

# How to do it?
Well, it is not that hard as you think or you might already know how to create a command alias temporarily. Anyway, here it goes...

First how create an alias ?

```bash
alias <command-alias-name>='command to be run'
```

The above given example is the syntax for creating a command alias. For a clear picture check the below command alias,

```bash
alias webroot='cd /var/www/projects'
```

run this on your terminal and run the command webroot on the terminal, your present working directory on the terminal will be changed to /var/www/projects and that’s how useful it is. But the problem is that when you run the alias command on the terminal the alias will be available on that particular terminal until it closes. How to make this permanent.

open the .bashrc file on your home directory 

```bash
vim ~/.bashrc
```

go to the end of the file and add the alias command and save the file.

go to your terminal and run the below command line,

```bash
source ~/.bashrc
```

tada!!! Now your command alias is available throught the terminals.

## **A cleaner way**

Yes, adding the command aliases to the .bashrc file can make it permanent but it can be a mess right? Let's do it in a more cleaner way

1. open the .bash_aliases file (create if doesn't exist)

```bash
vim ~/.bash_aliases
```

2. Enter your command aliases one by one and save it

3. Open .bashrc file

```bash
vim ~/.bashrc
```

4. Add the below entry to end of the line (some distros may have this entry by default)

```bash
source ~/.bash_aliases
```

5. Go to the terminal and run the below command.

```bash
source ~/.bashrc
```

Good Job.!!! You did it :) As simple as that

# Some useful aliases
```bash
alias addalias='vim ~/.bash_aliases'
alias ebrc='vim ~/.bashrc'
alias sapt='sudo apt-get'
alias apelog='sudo tailf /var/log/apache2/error_log'
alias httpdelog='sudo tailf /var/log/httpd/error.log'
alias nowdate='date +"%d-%m-%Y"'
alias docroot='/var/www/html'
alias vi=vim
alias svi='sudo vi'
```

>**NOTE: You can use any name instead of .bash_aliases**

Hope this helps you  :)

***Summary: Bash aliases can be used to create command shortcuts on the terminal. You can add the aliases to .bashrc/.bash_aliases file on the home directory.***