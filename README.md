# [rants.luispuerto.net][] source code

![](images/pages/homer-rant.jpg)

[![Netlify Status](https://api.netlify.com/api/v1/badges/03fa9854-e8d3-4018-9577-caf5453235ba/deploy-status)](https://app.netlify.com/sites/zen-villani-a013b8/deploys)
[![Jekyll](https://img.shields.io/badge/jekyll-4.0.0-blue.svg?logo=jekyll)][Jekyll]
[![GitHub](https://img.shields.io/github/license/luispuerto/rants.luispuerto.net?label=code%20license&logo=open-source-initiative&color=#3DA639)][LICENSE]
[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/content%20license-CC%20BY--NC--SA%204.0-lightgrey?logo=creative-commons)][LICENSE4CONTENT]

Welcomed to **Rants**!! This is a small sub-blog from my [main blog][luispuerto-net]. Here I pretend to rant about things that happen to me or things I really think are quite odd, weird, unfair or not working properly. 

Why ranting? Well, the question is. **Why not?**. Anyhow and first of all because venting out it good, and secondly, I really think of it as a way to give feedback. Feedback sometimes is the only tool we have to try to fix things that aren't under our control. 

<!-- MarkdownTOC -->

- [How this works?](#how-this-works)
    - [Configurations](#configurations)
    - [Deployment](#deployment)
    - [Posts](#posts)
    - [Pages](#pages)
    - [Navigation](#navigation)
    - [Disqus Comments](#disqus-comments)
    - [Google Analytics](#google-analytics)
    - [Social Media Links](#social-media-links)
    - [Update favicon](#update-favicon)
- [License](#license)

<!-- /MarkdownTOC -->

## How this works?

I'm using [Type][], from [Aspire Themes][], as a template. This is how it works this template. Spoiler alert!! I've done some modifications and additions, but I'll try to explain them in this Readme. 

### Configurations

Type theme comes with different customizations in the `_config.yml` file:

```sh
title:       Type
email:       ''
description: ''
baseurl:     '' # The subpath of your site, e.g. /blog
url:         '' # The base hostname & protocol for your site
twitter:     ''
github:      ''
instagram:   ''
facebook:    ''

markdown:  kramdown
permalink: pretty
paginate:  60

sass:
  style: compressed

gems:
  - jekyll-paginate
  - jekyll/tagging

include:
  - _pages

exclude:
  - vendor
  - Gemfile
  - Gemfile.lock

# Tags
tag_page_dir:         tag
tag_page_layout:      tag_page
tag_permalink_style:  pretty

# Pages path
defaults:
  - scope:
      path: '_pages'
    values:
      permalink: /:basename:output_ext
```

### Deployment

To run the theme locally, navigate to the theme directory and run `bundle install` to install the dependencies, then run `jekyll serve` to start the Jekyll server.

I would recommend checking the [Deployment Methods](https://jekyllrb.com/docs/deployment-methods/) page on Jekyll website.

### Posts

To create a new post, you can create a new markdown file inside the `_posts` directory by following the [recommended file structure](https://jekyllrb.com/docs/posts/#creating-post-files).

The following is a post file with different configurations you can add as an example:

```sh
---
layout: post
title: Welcome to Jekyll!
featured: true
tags: [frontpage, jekyll, blog]
image: '/images/welcome.jpg'
---
```

You can set the author, featured or not, tags, and the post image.

The `featured` key is to mark the post as a featured post, this will add a simple star icon (*) to the postcard.

To keep things more organized, add post images to **/images/pages** directory, and add page images to **/images/pages** directory.

To create a draft post, create the post file under the **_drafts** directory, and you can find more information at [Working with Drafts](http://jekyllrb.com/docs/drafts/).

For tags, try to not add space between two words, for example, `Ruby on Rails`, could be something like (`ruby-on-rails`, `Ruby_on_Rails`, or `Ruby-on-Rails`).

Note that tags are not working with GitHub Pages, that's because the used [jekyll-tagging
](https://github.com/pattex/jekyll-tagging) plugin is not [whitelisted](https://pages.github.com/versions/) by GitHub.

To make this work, I use [Netlify.com](https://www.netlify.com/) for deployment.

### Pages

To create a new page, just create a new markdown file inside the `_pages` directory.

The following is the `about.md` file that you can find as an example included in the theme with the configurations you can set.

```sh
---
layout: page
title: About
image: '/images/pages/about.jpeg'
---
```

Things you can change are: `title` and `image` path.


### Navigation

The navigation on the sidebar will automatically include all the links to the pages you have created.

### Disqus Comments

Maxima Theme comes with Disqus comments enabled.

Open `_includes/disqus.html` file, and change the `aspirethemes` value on line 15 with your [Disqus account shortname](https://help.disqus.com/customer/portal/articles/466208).

```js
s.src = '//aspirethemes-demo.disqus.com/embed.js';
```

So, if your Disqus shortname is `exampleone`, the final code above should be

```js
s.src = '//exampleone.disqus.com/embed.js';
```

That's all you need to setup Disqus from the theme side. If you get any issue regarding that comments are unable to load. First, make sure you have [registered your website with Disqus (Step 1)](https://help.disqus.com/customer/portal/articles/466182-publisher-quick-start-guide)

And also check [Disqus troubleshooting guide](https://help.disqus.com/customer/portal/articles/472007-i-m-receiving-the-message-%22we-were-unable-to-load-disqus-%22) if you still have issues.

### Google Analytics

To integrate Google Analytics, open `_includes/analytics.html`, and add your Google Analytics code.

### Social Media Links

Social media links included in `_includes/footer.html` file.

The theme is using [Evil Icons](http://evil-icons.io/), which contains very simple and clean icons. The following is a list of the social media icons to use:

Twitter

```html
<span data-icon='ei-sc-twitter' data-size='s'></span>
```

Facebook

```html
<span data-icon='ei-sc-facebook' data-size='s'></span>
```

Instagram

```html
<span data-icon='ei-sc-instagram' data-size='s'></span>
```

Pinterest

```html
<span data-icon='ei-sc-pinterest' data-size='s'></span>
```

Vimeo

```html
<span data-icon='ei-sc-vimeo' data-size='s'></span>
```

Google Plus

```html
<span data-icon='ei-sc-google-plus' data-size='s'></span>
```

SoundCloud

```html
<span data-icon='ei-sc-soundcloud' data-size='s'></span>
```

Tumblr

```html
<span data-icon='ei-sc-tumblr' data-size='s'></span>
```

Youtube

```html
<span data-icon='ei-sc-youtube' data-size='s'></span>
```

### Update favicon

You can find the current favicon (favicon.ico) inside the theme root directory, just replace it with your new favicon.

## License

The code of this project is under the MIT License —see the [LICENSE][] file for details. However, the content of the website is license under a Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International license ——see the [LICENSE4CONTENT][] file for details.


[rants.luispuerto.net]: https://rants.luispuerto.net
[Type]: https://github.com/aspirethemes/type
[Aspire Themes]: http://aspirethemes.com
[luispuerto-net]: https://luispuerto.net 
[LICENSE]: LICENSE
[LICENSE4CONTENT]: LICENSE4CONTENT.txt
[Jekyll]: https://jekyllrb.com
