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

# Posts

### Adding Posts

From Jekyll's documentation:

To create a new post, all you need to do is create a file in the `\_posts` directory. How you name files in this folder is important. Jekyll requires blog post files to be named according to the following format:

```
YEAR-MONTH-DAY-title.MARKUP
```
Where `YEAR` is a four-digit number, `MONTH` and `DAY` are both two-digit numbers, and `MARKUP` is the file extension representing the format used in the file. Here are some examples:

```
2018-08-14-welcome-to-jekyll.markdown
2018-08-30-example.md
```

Be sure to write front-matter, typically including a `title`, `layout`, publishing `date`, and `tags`.

```
---
layout: post
title: "Welcome to Jekyll!"
date: 2015-11-17 16:16:01 -0600
tags: update
---
```

The format for date is `YEAR-MONTH-DATE` `HOUR:MINUTE:SECOND` `TIMEZONE`.

### Making Tags

[Jekyll's explanation on how to create categories](https://jekyllrb.com/docs/posts/#displaying-post-categories-or-tags) can be used to make tags.

When making new tags, create a new markup file under the directory `tags`. For example, if you have a new tag `blog`, then createa file under the `tags` directory, such as `blog.html` or `blog.md` with at least

```
---
layout: tag
title: #blog
tag: blog
---
```

# Pages

### Creating A Page

* Create an .md or .html file in the`pages` folder. You can also create the file in the root directory.
* Name the file with the intended page link. For example, if you what the URL to be `/url`, then name the file `url.md` or `url.html`.
* Write the front-matter for the page.

```
---
layout: page
title: String // Title of the Webpage
permalink /String/ // Permalink of the Webpage
---

---
layout: page
title: "Example Title"
permalink: /example/
---
```


