jekyll-caption-tag
==================

A Liquid tag for Jekyll sites that allows easy creation of captioned
images like they are in WordPress.

How To Install
===============
1. Install all required gems: `dimensions`, `rmagick` (`sudo gem install dimensions rmagick` on Debian-based machines)
2. Copy `caption_tag.rb` into `<your-jekyll-site>/_plugins`.
3. Add the styles from `style.css` to your stylesheets.

How To use
==========
Place a `caption` tag in your content file, e.g.:
```
{% caption align="aligncenter" width="512" height="233" alt="The order of points is important for the definition of a polygon" text="[A, B, C, D, E, F, G] != [A, B, C, D, F, E, G]" url="../images/2013/11/polygon-order.png" %}
```

| Attribute     | Details                                                                    |
| ------------- |--------------------------------------------------------------------------- |
| align         | The content of this will be added to the class of the surrounding `<div>`. |
| width         | The width of the image.                                                    |
| height        | The width of the image.                                                    |
| alt           | The alternative attribute for images.                                      |
| caption       | The text below the image.                                                  |
| url           | The source (src) of the image.                                             |

Examples
========
* [post](https://github.com/MartinThoma/MartinThoma.github.io/blob/source/_posts/2013-11-18-check-point-inside-polygon.md), [rendered post](http://martin-thoma.com/check-point-inside-polygon/)

Changelog
=========
Version 1.4, 2014-03-27:
    - Fixed issue (if two files had the same name, but were in different folder the captions were overwritten)
Version 1.3, 2014-03-24:
    - Captions can resizes automatically to a given maximum size while preserving the aspect ratio.
Version 1.2, 2014-01-07:
    - The enclosing `div` is now 10px wider than the `img` inside.
Version 1.1, 2014-01-07:
    - Just take the URL that was given, don't add anything.
    - Close image tag
Version 1.0, 2014-01-02: Initial commit.

License
=======
This code is licensed under MIT License. 

What does this mean?

* You may use it if you like
* Don't blame me when thinks don't work (though you can file an issue)
* Please don't remove the link in the comments of `caption_tag.rb`.
  This might help others to find this plugin
