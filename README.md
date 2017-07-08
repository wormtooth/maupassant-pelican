# Maupassant

A pelican theme ported from [maupassant-hexo](https://github.com/tufu9441/maupassant-hexo) by [tufu9441](https://github.com/tufu9441), which originated from [maupassant](https://github.com/pagecho/maupassant/) by [cho](https://github.com/pagecho).

## Installation

`cd` into your blog folder. Then

```bash
git clone https://github.com/wormtooth/maupassant-pelican ./maupassant
```

Then change/add `THEME` option in `pelicanconf.py` to

```python
THEME = 'maupassant'
```

## Options

### Navigation Menu

`MENUITEMS`: It is a list of tuples in the format of
<center>(title, link, [font-awesome-id](http://fontawesome.io/))</center>
The default value of `MENUITEMS` is

```python
MENUITEMS = [('Home', '.', 'fa-home'), ('Archive', 'archives.html', 'fa-archive')]
```

**WARNING**: You should/must always put ('Home', '.', 'fa-home') as a menu item.

### Widgets

`WIDGETS`: It is a list of strings representing the widgets, which can be found in the **template/widgets** folder.

```python
WIDGETS = ['search', 'category', 'tag', 'recent_articles', 'recent_comments', 'links']
```

#### Available widgets

- 'search': google search for the blog.
- 'category': show a list of current categories.
- 'tag': show 100 current tags. Can be used with plugin [tag cloud](https://github.com/getpelican/pelican-plugins/tree/master/tag_cloud).
- 'recent_articles': show recent 10 articles.
- 'recent_comments': show recent 5 comments. Display only if `DISQUS_SHORTNAME` is set.
- 'links': blogroll. You can customize it via `LINKS`.

You can make your own widgets by creating a corresponding html file in the **template/widgets**folder. Then you can activate it by putting its name into `WIDGETS`.

### Comments

Only Disqus commenting system is supported right now. 

`DISQUS_SHORTNAME`: It is a string representing your Disqus shortname. 

Comments by default are enabled for articles and are closed for pages. You can enable/disable comments on certain articles or articles by providing `comments` keyword in the front matter. 

To enable: `comments: True`

To disable: `comments: False`

### Math Rendering

`MATHJAX`: `True` or `False`(default). Better to have plugin [render math](https://github.com/getpelican/pelican-plugins/tree/master/render_math) installed also.

### Syntax Highlight Style

The default syntax highlight style is `default`. If you want to change the style, you can change the `pygment.css` file in **static/css** folder. See Pelican official [FAQ](http://docs.getpelican.com/en/3.6.3/faq.html#i-m-creating-my-own-theme-how-do-i-use-pygments-for-syntax-highlighting) if you want to use other styles.

### Logo

The theme can recognize **favicon.ico** in its theme folder. So put your logo in the theme folder if you want to have it used on your website.

### Summary of Article

If `<!--more-->` is put somewhere in an article, article content until `<!--more-->` will be used as summary shown on index pages. If there is no such tag, `article.summary` will be used.

## Maupassant on other platforms:
- Typecho：[https://github.com/pagecho/maupassant/](https://github.com/pagecho/maupassant/)
- Octopress：[https://github.com/pagecho/mewpassant/](https://github.com/pagecho/mewpassant/)
- Farbox：[https://github.com/pagecho/Maupassant-farbox/](https://github.com/pagecho/Maupassant-farbox/)
- Ghost: [https://github.com/LjxPrime/maupassant/](https://github.com/LjxPrime/maupassant/)