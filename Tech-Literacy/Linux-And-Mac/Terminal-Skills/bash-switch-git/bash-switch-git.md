# Using a Bash Script to Switch Git Profiles

## Table of Contents

1. [Overview](#overview)
2. [Explanation](#explanation)
3. [Resoureces](#resoureces)

---

## Overview

So, you got your first software engineering job, and now you need to connect one laptop to two git accounts with their own ssh keys. While, there is enough documentation on this, I have still find myself spending more time than I would like setting this up, particularly if you need to connect to GitHub Enterprise with an unknown hostname(s).

The conventional way to fix this is to just modify the <code>config</code> file in the <code>.ssh</code> directory.

Free Code Camp has an excellent [article](https://www.freecodecamp.org/news/manage-multiple-github-accounts-the-ssh-way-2dadc30ccaca/) on this topic if you need a full walk-through on how git works alongside ssh.

In the article, you will see where they show the recommended config file for having multiple git account with their own ssh key:

![normal config file](normalConfig.png)

Personally, this method wasn't doing it for me because when you clone a repo with ssh, you have to remember and manually change the hostname in the url to match the hostname you used in the config file.

So, what do we do when there is a minor inefficiency in our daily tech workflow? A: We severely overcomplicate the solution and spend a few hours writing a BASH script, naturally!

---

## Explanation

Here's what I came up with - let's break it into pieces:

![bash script](bashScript.png)

1. shebang
2. global variables/ parameters
3. show me the file before the script
4. script logic
5. show me the file after the script

---

## Resources
