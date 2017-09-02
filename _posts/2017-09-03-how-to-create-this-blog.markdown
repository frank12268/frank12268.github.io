---
layout: post
title:  "How to Create This Blog"
date:   2017-09-03 01:24:41 +0800
categories: github
tags: [github, jekyll]
---
## Install Jekyll
```
brew install ruby
sudo gem install jekyll
sudo gem install bundler
```
## Create git repository for github pages
Create a git repository with the name of `<username>.github.io` and checkout.
```
git clone https://frank12268@github.com/frank12268/frank12268.github.io.git
```
## Create a jekyll blog
```
cd frank12268.github.io
jekyll new blog
cp blog/* ./
rm -fr blog/
```
## Post new blog
> You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `jekyll serve`, which launches a web server and auto-regenerates your site when a file is updated.

> To add new posts, simply add a file in the `_posts` directory that follows the convention `YYYY-MM-DD-name-of-post.ext` and includes the necessary front matter. Take a look at the source for this post to get an idea about how it works.

## TODO change layout

## TODO create category and tag block

## Reference
[github pages](https://pages.github.com/)

[New Creation](http://www.devtalking.com/articles/git-gitHub-markdown-jekyll/)

[Category & Tag](https://codinfox.github.io/dev/2015/03/06/use-tags-and-categories-in-your-jekyll-based-github-pages/)