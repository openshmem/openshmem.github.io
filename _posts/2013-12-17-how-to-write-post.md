---
layout: post
title: How to write post
author: intijk
---

This document is used for describing how write post to this blog. 

I assume you already have the knowledge about [Markdown](http://daringfireball.net/projects/markdown/) and git.


Step 1: Checkout repo
---
Checkout the repo on github by SSH:

```bash
git clone git@github.com:openshmem/openshmem.github.io.git
```
   

Step 2: Make your content
---
*_posts* directory contailns all the posts data, what you need to do is write your post there. What need to notice is filename of your post is important, it must be:

	year-month-day-my-post-title.md

Add these lines whenever you start a new post.

	---
	layout: post
	title: post title
	author: your name or id
	---

And start your post content under it.

Step 3: Do local test
---
To test your post, you need *ruby* and *jekyll*, the jekyll version for this repo is 1.9, you can install these tools in source. For example, you can do this under openSUSE:

```bash
sudo zypper in ruby ruby-devel
gem install jekyll
```

Then run *jekyll serve* under your repo directory, for example in my machine:

```bash
cd openshmem.github.io
jekyll1.9 serve
```
This will start a process listening on localhost:4000 as a webserver. Use your browser to check the result.

Step 4: Commit
---
If everything looks fine, what you need is to commit your change. Just git add the markdown file and push. **git add and only add the file you created or edited** , don't touch any other files. 

```bash
git add _posts/year-month-day-title.md
git push
```
You are done! Feel free to add any content about research ideas, programming,  application configuration, etc.  :-)

