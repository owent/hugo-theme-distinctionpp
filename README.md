# distinctionpp

Distinctionpp theme for [Hexo].

- [Preview](https://owent.net/)

## Installation

### Install

``` bash
$ git clone -b master https://github.com/owt5008137/hugo-theme-distinctionpp.git themes/distinctionpp
```

**Distinctionpp requires Hexo 2.4 and above.**

### Enable

Modify `theme` setting in `_config.yml` to `distinctionpp`.

### Update

``` bash
cd themes/distinctionpp
git pull
```

## Configuration

``` yml
# Header
menu:
  Home: /
  Archives: /archives
rss: /atom.xml

# Content
excerpt_link: Read More
fancybox: true

highlight:
  enable: false         # set false to use highlight.js in client mode
  style: "default"      # style name
  langs: ['capnproto', 'cmake', 'd', 'dos', 'erlang', 'go', 'less', 'lua', 'php', 'powershell', 'protobuf', 'profile', 'typescript', 'vim'] # extend languages
  selector: 'pre>code'  # How to find code
  url:                  # Where to import highlight.js, all configure in highlight are available
    js: "//cdnjs.cloudflare.com/ajax/libs/highlight.js/<%- version %>/highlight.min.js"
    style: "//cdnjs.cloudflare.com/ajax/libs/highlight.js/<%- version %>/styles/<%- style %>.min.css"
    lang: "//cdnjs.cloudflare.com/ajax/libs/highlight.js/<%- version %>/languages/<%- lang %>.min.js" # for (let lang of langs) 
  options:              # options of highlight.js see http://highlightjs.readthedocs.io/en/latest/api.html#configure-options
    tabReplace: '    '
    useBR: false
    #classPrefix: 'hljs-'
    languages: {}   # language alias

widgets:
- category
- tag
- tagcloud
- archives
- recent_posts

# Miscellaneous
google_analytics:
favicon: /favicon.png

# where to import jquery
jquery:
  js: //code.jquery.com/jquery-3.2.1.min.js
  migrate: //code.jquery.com/jquery-migrate-1.4.1.min.js

# where to import bootstrap
bootstrap:
  js: //cdnjs.cloudflare.com/ajax/libs/twitter-bootstrap/4.0.0-alpha.6/js/bootstrap.min.js
  css: //cdnjs.cloudflare.com/ajax/libs/twitter-bootstrap/4.0.0-alpha.6/css/bootstrap.min.css

# where to import fancybox
fancybox:
  enable: true
  js: //cdnjs.cloudflare.com/ajax/libs/fancybox/3.1.20/jquery.fancybox.min.js
  css: //cdnjs.cloudflare.com/ajax/libs/fancybox/3.1.20/jquery.fancybox.min.css

disqus_shortname:     # disqus shortname for inserting comments
disqus_on_page: false # if insert disqus in pages

gitment: # use https://github.com/imsun/gitment for comments
  enable_on_page: false
  js: https://imsun.github.io/gitment/dist/gitment.browser.js
  css: https://imsun.github.io/gitment/style/default.css
  owner: owent
  repo: 'blog-comment'
  oauth:
    client_id: 
    client_secret: 
```

- **menu** - Navigation menu
- **rss** - RSS link
- **excerpt_link** - "Read More" link at the bottom of excerpted articles. `false` to hide the link.
- **fancybox** - Enable [Fancybox]
- **widgets** - Widgets displaying in archives
- **google_analytics** - Google Analytics ID
- **favicon** - Favicon path

## Features

### Fancybox

Distinctionpp uses [Fancybox] to showcase your photos. You can use Markdown syntax or fancybox tag plugin to add your photos.

```
![img caption](img url)

{% fancybox img_url [img_thumbnail] [img_caption] %}
```

All of them are enabled by default. You can edit them in `widget` setting.

## Development

