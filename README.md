jekyll-caption-tag
==================

A Liquid tag for Jekyll sites that allows easy creation of captioned
images like they are in WordPress.

How To Install
===============
1. Copy `caption_tag.rb` into `<your-jekyll-site>/_plugins`.
2. Add the styles from `style.css` to your stylesheets.

How To use
==========
Place a `caption` tag in your content file, e.g.:
```
{% caption align="aligncenter" width="512" height="233" alt="The order of points is important for the definition of a polygon" text="[A, B, C, D, E, F, G] != [A, B, C, D, F, E, G]" url="../images/2013/11/polygon-order.png" %}
```

Examples
========
* [post](https://github.com/MartinThoma/MartinThoma.github.io/blob/source/_posts/2013-11-18-check-point-inside-polygon.md), [rendered post](http://martin-thoma.com/check-point-inside-polygon/)

Changelog
=========
Version 1.0, 2014-01-02: Initial commit.

License
=======
This code is licensed under MIT License. 

What does this mean?

* You may use it if you like
* Don't blame me when thinks don't work (though you can file an issue)
* Please don't remove the link in the comments of `caption_tag.rb`.
  This might help others to find this plugin
