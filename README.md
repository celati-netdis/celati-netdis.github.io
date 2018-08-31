# Dependencies

This website uses Jekyll and its built-in SCSS compiler for the associated CSS, so be sure to install Jekyll first.

```bash
$ gem install jekyll
```

If you don't have the `bundler` gem installed, you can install it this way:

```bash
$ gem install bundler
```

More information on how to install and quick start Jekyll can be found [here](https://jekyllrb.com/docs/installation/) and [here](https://jekyllrb.com/docs/quickstart/).

This website also uses Bootstrap, JQuery, and Popper.JS for stylization purposes. Documentation on them can be found [here](https://getbootstrap.com/docs/4.1/getting-started/introduction/), [here](https://api.jquery.com/), and [here](https://popper.js.org/popper-documentation.html). Here is also [a guide on how to add Bootstrap](https://simpleit.rocks/ruby/jekyll/tutorials/how-to-add-bootstrap-4-to-jekyll-the-right-way/) to Jekyll.

# Adding Posts

From Jekyll's documentation:

To create a new post, all you need to do is create a file in the \_posts directory. How you name files in this folder is important. Jekyll requires blog post files to be named according to the following format:

```
YEAR-MONTH-DAY-title.MARKUP
```
Where YEAR is a four-digit number, MONTH and DAY are both two-digit numbers, and MARKUP is the file extension representing the format used in the file. Here are some examples:

```
2018-08-14-welcome-to-jekyll.markdown
2018-08-30-example.md
```

Be sure to write front-matter, typically including a title, layout, publishing date, and tags.

```
---
layout: post
title: "Welcome to Jekyll!"
date: 2015-11-17 16:16:01 -0600
tags: update
---
```

### Making Tags

x

# Creating Pages

