+++
title = "Hugo with emacs org mode"
author = ["Prasad Ghole"]
date = 2022-11-07T00:00:00+05:30
layout = ""
linkTitle = ""
markup = ""
slug = ""
tags = ["Hugo"]
type = "post"
url = ""
draft = false
+++

{{< figure src="/images/post/org-mode-qt.jpg" >}}


## Why {#why}

Exclusively using emacs for writing documentation. I can now write posts directly in org mode.


## Advantages {#advantages}

-   Never leave emacs.
-   Template with all the hugo parameters
-   Override or customize front matter.


## Basic Setup {#basic-setup}

For my hugo even theme when I create post using new command front matter is already inserted. Below are customization options


### Hugo project path {#hugo-project-path}

We need to specify hugo project path this can be relative

{{< highlight nil >}}
#+hugo_base_dir: ../../
{{< /highlight >}}

This is hard coded. Find way to make it based on environment Find way to make it based on environment.


### Front matter configuration {#front-matter-configuration}

{{< highlight nil >}}
#+hugo_front_matter_format: toml
{{< /highlight >}}


### Export path {#export-path}

{{< highlight nil >}}
#+hugo_section: post
{{< /highlight >}}


### TOC {#toc}

{{< highlight nil >}}
#+hugo_front_matter_format: toc false
{{< /highlight >}}


### Credits {#credits}

[Freepik](https://www.freepik.com/free-vector/cyber-security-concept%5F7970729.htm#query=cybersecurity&position=1&from%5Fview=search&track=sph)

