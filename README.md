# What is this.

This is the grid based theme for Hugo.

[Hugo :: A fast and modern static website engine](https://gohugo.io/)

## PC View

![screenshot](https://raw.githubusercontent.com/dim0627/hugo_theme_robust/master/images/screenshot.png)

## SP View(Responsive)

![screenshot](https://raw.githubusercontent.com/dim0627/hugo_theme_robust/master/images/responsive.png)

# Features

* [Accelerated Mobile Pages Project](https://www.ampproject.org/) a.k.a AMP supported
* Responsive design
* Google Analytics
* Thumbnail
* Share button
* Structured data(Article and Breadcrumb)
* Twitter cards
* OGP
* Disqus
* Syntax Highlight

## Installation

```
$ cd themes
$ git clone https://github.com/dim0627/hugo_theme_robust.git
```

[Hugo \- Installing Hugo](http://gohugo.io/overview/installing/)

# `config.toml` example

```
baseurl = "https://example.com/"
title = "SiteTitle"
theme = "hugo_theme_robust"

googleAnalytics = "UA-XXXXXXXX-XX" # Optional
disqusShortname = "XYW"

[params]
  description = "This is site description"
  dateformat = "Jan 2, 2006" # Optional
  # Fonts settings.
  googlefonts = "https://fonts.googleapis.com/css?family=Lobster|Lato:400,700" # Optional, Include google fonts.
  fontfamily = "Lato,YuGothic,'Hiragino Kaku Gothic Pro',Meiryo,sans-serif" # Optional, Override body font family.
  logofontfamily = "Lobster, cursive" # Optional, Override logo font.

[params.author]
  thumbnail = "images/author.jpg"
  name = "John Doe"
  description = "<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit</p><p>sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>"
  facebook = "https://www.facebook.com/daisuke.tsuji.735"
  twitter = "https://twitter.com/dim0627"
  github = "https://github.com/dim0627"

[outputs]
page = [ "HTML", "AMP" ] # if you want AMP enable.
```

# Frontmatter example

```
+++
date = "2016-09-28T17:00:00+09:00"
title = "Article title here"
thumbnail = "images/thumbnail.jpg" # Optional, referenced at `$HUGO_ROOT/static/images/thumbnail.jpg`
toc = true # Optional
+++
```

# Shortcodes

## Image

```
{{% img src="images/image.jpg" w="600" h="400" %}}
{{% img src="images/image.jpg" w="600" h="400" caption="Referenced from wikipedia." href="https://en.wikipedia.org/wiki/Lorem_ipsum" %}}
```

![screenshot](https://raw.githubusercontent.com/dim0627/hugo_theme_robust/master/images/include-images.png)

# Development mode

Supported development mode.

```
env HUGO_ENV="DEV" hugo server --watch --buildDrafts=true --buildFuture=true -t robust
```

This mode is

* Not show Google Analytics tags.
* Show `IsDraft`.
* Show `WordCount`.

And set `{{ if ne (getenv "HUGO_ENV") "DEV" }} Set elements here. {{ end }}` if you want to place only in a production environment.

