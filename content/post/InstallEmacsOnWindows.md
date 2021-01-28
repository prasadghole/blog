+++
author = "Prasad Ghole"
date = 2021-01-26
title = "Installing spacemacs on windows"
tags = [
"vim"
]
categories = [
"development",
]
+++
# Installing spacemacs on windows
Once we install vanilla emacs from gnu website we want to do  little  twick for  running emacs configuration when  we
run runemacs.exe command.

We need to find out where is  emacs startup home directory path.  

## Finding  startup directory 

Check user  emacs directory 
{{<highlight bash "hl_lines=1 " >}}
CTRL-H  v 
{{</highlight >}}
Enter variable name
{{<highlight bash "hl_lines=1 " >}}
user-emacs-directory
{{</highlight >}}


## Cloning spacemacs configuration 
When ever emacs starts it looks for startup directory in  user emacs directory found above.  We will get 
that configuration directly from github.com.


{{<highlight bash "hl_lines=1 " >}}
git clone https://github.com/syl20bnr/spacemacs C:\%USERPROFILE%\appdata\roaming\.emacs.d
{{</highlight >}}

### Job well done
Enjoy
