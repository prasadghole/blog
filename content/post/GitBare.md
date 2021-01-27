+++
author = "Prasad Ghole"
date = 2020-07-29
title = "Git in a box"

tags = [
"git",
]

categories = [
"development",
]
+++
# Git in a box 
Github is certailnly a good source of keeping master copy of your decentralized git repo. But in some 
scenario project thing it would be much better to have git repository as portable copy.This is where 
git bare repository helps.

## Bare repository
A bare repository is one without working copy. We can push or pull our changes to/from this repo. We
can keep this repository portable and handy. Can be mount on shared drive and your github is done.
{{<highlight C "hl_lines=1 " >}}
git init --bare 

{{</ highlight >}}
## Using bare repository
We can push existing repo to this file based repository similar to remote repository.

{{<highlight C "hl_lines=1 " >}}
git push <path of bare repo> master

{{</ highlight >}}
We can clone this bare repository similar to our github repo
{{<highlight C "hl_lines=1 " >}}
git clone <path of bar repository> <clone directory>
{{</ highlight >}}



