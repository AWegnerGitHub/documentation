Title: Few more features of Elegant
Tags: pelican-theme, web-design
Category: Elegant - Pelican Theme
Date: 2014-04-22 16:23
Slug: few-more-features-of-elegant
Disqus_identifier: c8et6bu-few-more-features-of-elegant
Subtitle:
Summary: Three more features that are unique to Elegant theme
Keywords:

[TOC]

Here are few more features that make Elegant a unique and powerful theme for
Pelican powered blogs.

## Add License to your Site

You can put your license string in `SITE_LICENSE`. It will appear in the footer
of every page of your site. Here is how license of my site looks like,

![onCrashReboot site license](|filename|/images/elegant-theme_license.png)

## Site Subtitle

You can also define `SITE_SUBTITLE`, it appears in the footer, before site
license.

![Site subtitle](|filename|/images/elegant-theme_site-subtitle.png)

## Web Safe Fonts

Elegant uses commonly available typefaces in every style rule. It has a list of
closely matching fonts in the fallback list. For examples Baskerville is the
first choice for headings. But if reader does not have Baskerville installed,
Garamond will be used. If that too fails then Georgia will be used.

## Adding Author Blurbs

At the end of each article, you can provide a small blurb about the author. This
can be done by setting up the `AUTHORS` dictionary in your configuration file.

    :::python
    AUTHORS = {
        u'Talha Mansoor': {
            u'blurb': """ created Elegant Pelican theme, dabbles in Python, Vim-L and JavaScript. They can be reached on Github, Twitter and email.""",
            u'url': 'https://github.com/talha131/'
        },
    }

Add an entry for each author you'd like a blurb to appear for.

These blurbs will appear for each known author, as defined in the `AUTHORS`
dictionary. If an unknown author appears, they will not receive a blurb.

The article author is determined by the provided metadata in your content
file. Valid values are:

    - `author:` - This defines the *single* author of the article.
    - `authors:` - This is a comma separated list of all article authors. Each
    known author will get a blurb. Each unknown author will not get a blurb.
    - Default author defined in your configuration file. If either of the two
    metatags above are not used, the default author you configured will be
    utilized. This author still requires an entry in the `AUTHORS` dictionary.

**Note:** If you define multiple authors, but use the `author:` metatag, a blurb
will not be generated. This metatag is for a *single* author. The correct way to
declare more than one author is to use `authors:`.

This is an example of multiple authors using the following metatag value:

    :::python
    authors: Talha Mansoor, Milton Bradley

![Author Blurb](|filename|/images/author-blurb.png)
