---
layout: post
title: "Testing Jekyll Versions"
date:   2022-03-10 13:43:31 -0400
categories: jekyll update
---

A lot of what we are learning in Digital Humanities Research is how to build things and then break them apart to try to figure out all the parts. Today I worked with the tech team to figure out how to isolate the front matter of the index page from the posts page, which I had previously done by completely deleting the sample post. Today, I wanted to add a header page with the post feed in it. So the solution eventually was to create a layouts folder for the minima theme, which is not included if you install from the command line. Once I did that, I went on Github and copied over the home layout, which I used for the front matter/index page, and deleted all the functions for running the feed. Then I created a new layout called postdefault, in which I duplicated the home layout from the Github page as is. Then I create a Post.markdown page, using the postdefault layout. I also added the posts.markdown page as a header page in the config file. The result is a static front page, which is essentially an About page, then a posts page in the header that incudes the feed. Voila!  
