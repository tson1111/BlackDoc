---
layout: post
title: [Tech]Hello, World!
---

## Prologue

**Hello, world!**       

——According to the tradition of coders, this is my first post on my blog. 

After 7 or 8 hours working and running into a looooot of problems, I finally completed the initial work of building the website. The next step is to maintain and update my blog to keep it alive. Wish me good luck!  

## Problem Solving

I was building the website with win10 OS and jekyll. The following is some problems I went through.

1. Install ruby and devkit. You need to install all these stuffs and click all of them during installation.

2. Install jekyll. gem install jekyll would be OK if you done the ruby and devkit thing right.

3. Choose a satisfying theme. Choose the **new** ones!! Make sure it isn't out of date so that someone still maintains it. In that case there will not be any problems I will describe later. 

4. Install bundler. Many themes need bundler. When installing, make sure the version is in conformity with the theme (check *Gemfile.lock*).

5. Git stuff as normal.

6. Jekyll Usage: 

   ```bash
   bundle install
   bundle exec jekyll server (--watch)
   bundle exec jekyll build
   ```

7. HTTPS or HTTP. Some old themes uses font via http protocol website, and this may cause the theme looks differently from local server. In this case, try to replace all the "http" with "https" in the html file. It works for me.



