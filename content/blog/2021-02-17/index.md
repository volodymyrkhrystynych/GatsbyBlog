---
title: Learning to code in Spacemacs
date: "2021-02-20"
description: How I fumbled my way through learning to code in spacemacs
---

This started a while ago when I first got into vim, or more specifically neovim. The reason that I started using vim-like editors was because I bought a gpd-pocket in order to act as a pocket pc/journaling device and while windows ran well on it the "mouse" was mediocre at best and I found that editing files using vim in the powershell was most of what I was doing on it. So I switched to a linux distro, got a window manager as I didn't have enough space to resize windows as got to work. I got a developement environment to work in neovim using plugins but found myself constantly trying to emulate and find different plugins that do what I want in neovim, this became tedious and so I decided to try out spacemacs.

## Problem 1: 

While trying to code a blog in gatsbyjs the development script kept crashing due to something emacs would put beside the file when you change it but before you save. The solution was found here:

https://github.com/gatsbyjs/gatsby/issues/16054

Apperantly it was a link instead of an actual file. The solution that worked for me was adding this line to my dotfile.

(setq create-lockfiles nil)

I tried to configure the gatsby-config to ignore the .#myfile files but that didn't work no matter what I put in the ignore secion and just making emacs not spawn these files, seems to be the best solution as it will work into the future.


## Getting magit to work:

https://develop.spacemacs.org/layers/+source-control/git/README.htmL

The standard action of stage all, commit and push changes in git:

space-g-s // to open git status.
S         // to stage all changes.
c-c       // Now you write a commit message.
Z-Z       // Save commit message and commit changes.


## How to get a filetree to open

space-p-t // toggles treemacs, need to figure out how to remove projects from it

## Things that need to be investigated:

How to open projects more easily, or to get projects to show up when doing the projectile-helm command (space-p-h).
