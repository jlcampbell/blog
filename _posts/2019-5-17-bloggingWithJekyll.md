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

4. now, create a file named "index.html" under root
```
---
layout: default
title: Home
---
<h1>Latest Posts</h1>

<ul>
  {% for post in site.posts %}
    <li>
      <h2><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h2>
      <p>{{ post.excerpt }}</p>
    </li>
  {% endfor %}
</ul>
```
