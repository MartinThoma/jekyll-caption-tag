jekyll-caption-tag
==================

A Liquid tag for Jekyll sites that allows easy creation of captioned
images like they are in WordPress.

How To Install
===============
1. Install all required gems: `dimensions`, `rmagick` (`sudo gem install dimensions rmagick` on Debian-based machines)
2. Copy `caption_tag.rb` into `<your-jekyll-site>/_plugins`.
3. Add the styles from `style.css` to your stylesheets.
4. The thumbnails get created in `<your-jekyll-site>/captions`. 
   Make sure that you don't use this folder.
5. After every site generation, move `<your-jekyll-site>/captions` to
   `<your-jekyll-site>/_site/captions`.

How To use
==========
Place a `caption` tag in your content file, e.g.:
```
{% caption align="aligncenter" width="512" height="233" alt="The order of points is important for the definition of a polygon" caption="[A, B, C, D, E, F, G] != [A, B, C, D, F, E, G]" url="../images/2013/11/polygon-order.png" %}
```

| Attribute     | Details                                                                    |
| ------------- |----------------------------------------------------------------------------|
| align         | The content of this will be added to the class of the surrounding `<div>`. |
| width         | The width of the image.                                                    |
| height        | The width of the image.                                                    |
| alt           | The alternative attribute for images.                                      |
| caption       | The text below the image.                                                  |
| url           | The source (src) of the image.                                             |

Global configuration options
============================

You can place the following options in your `_config.yml` file:

| Attribute          | Default     | Details                                                         |
|--------------------|-------------|-----------------------------------------------------------------|
| caption_max_width  | "512"       | The maxiumum width captions may have when you don't specify it. |
| caption_max_height | "800"       | The maximum height captions may have when you don't specify it. |
| caption_folder     | "/captions" | The folder where captions get stored.                           |

Examples
========
* [post](https://github.com/MartinThoma/MartinThoma.github.io/blob/source/_posts/2013-11-18-check-point-inside-polygon.md), [rendered post](http://martin-thoma.com/check-point-inside-polygon/)

Changelog
=========
* Version 1.8, 2014-04-18:
    - Check and fail if url attribute is missing.
    - Fix for a problem that occured when image was smaller than the specified
      width.
* Version 1.7, 2014-04-18:
    - Relative URLs check path relative to the pre-generation post first.
      If no image is found then the root source folder is taken as base.
    - Fixed get_online_url to use the caption folder (see issue #6).
* Version 1.6, 2014-04-18:
    - Fixed issue (generated caption images were not used)
* Version 1.5, 2014-04-13:
    - Added global configuration options
    - Added check if image was already scaled
    - Added logger
* Version 1.4, 2014-03-27:
    - Fixed issue (if two files had the same name, but were in different folder the captions were overwritten)
* Version 1.3, 2014-03-24:
    - Captions can resizes automatically to a given maximum size while preserving the aspect ratio.
* Version 1.2, 2014-01-07:
    - The enclosing `div` is now 10px wider than the `img` inside.
* Version 1.1, 2014-01-07:
    - Just take the URL that was given, don't add anything.
    - Close image tag
* Version 1.0, 2014-01-02: Initial commit.

License
=======
This code is licensed under MIT License. 

What does this mean?

* You may use it if you like
* Don't blame me when thinks don't work (though you can file an issue)
* Please don't remove the link in the comments of `caption_tag.rb`.
  This might help others to find this plugin

Documentation
=============
I have a [generated rdoc documentation](https://rawgithub.com/MartinThoma/jekyll-caption-tag/master/doc/index.html).

It was generated with this command:

```bash
rdoc --exclude=/doc
```

TODO
====
* Try to get rid of step 5 of "how to install".