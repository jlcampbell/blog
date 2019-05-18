---
layout: post
title: Blogging with Jekyll on Github
---

How to make a totally free, totally controlled by you blog using github
** it is harder than it should be but I'm here to help

1. create a new repository in github, and initialize with readme

2. in settings, scroll down to the github pages section and select in the source tab "master branch"
.2 .a. choose a theme with the theme chooser

at this point you have a working site at https://[yourusername].github.io/[repoName]

3. your repo should have 2 files now, a README, and a config.yml. keep these. you will add 4 more files including your first blog post!

4. create a file named "index.html" under root

5. create a directory each : _layouts _data _posts

6. in _layouts, copy this file: https://github.com/jlcampbell/blog/blob/master/_layouts/post.html

7. in _data, create navigation.yml and paste this:
```
- name: Home
  link: /
```
8. create a new post in _posts called [year]-[month]-[day]-[title].md
. 8 .a. at the top, put this:
```
---
layout: post
title: Blogging with Jekyll on Github
---
```

below, put whatever markup you want.

When you launch your site you should see a link to your post! Any new posts you add to the posts directory will show up on your site now!



