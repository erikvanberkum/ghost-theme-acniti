# ghost theme acniti

Ghost theme acniti is based on a modified verion of the Editorial theme, a news-oriented design built around a dynamic 'locking' sidebar (try the toggle to see it in action!) and purpose built for content-centric sites. Originally created by [@ajlkn](https://twitter.com/ajlkn) for [HTML5 UP](https://html5up.net) and later ported to [Ghost](https://ghost.org)

- **Demo of the English Ghost acniti theme https://h2.acniti.com/**
- **Demo of the Dutch Ghost acniti theme https://h2.acniti.com/nl/**
- **Demo of the Spansh Ghost acniti theme https://h2.acniti.com/es/**
- Demo original site: https://editorial.ghost.io


![screenshot](https://github.com/erikvanberkum/ghost-theme-acniti/blob/master/assets/h2_acniti_front_page_900.jpg) 

# multi language

To make a ghost site work in multi language the routes.yaml file needs to be modified
The file located in: content / settings / routes.yaml

paste the following or modify if other languages required

```
routes:
  /about/:
    data: page.about
    template: index
  /over-ons/:
    data: page.over-ons
    template: index-nl
  /sobre-nosotros/:
    data: page.sobre-nosotros
    template: index-es
  /pricing/:
    data: page.pricing
    template: index
  /prijzen/:
    data: page.prijzen
    template: index-nl
  /precios/:
    data: page.precios
    template: index-es

collections:
  /:
    permalink: /{slug}/
    template: index
    filter: 'tag:-[hash-nl,hash-es]'
  /nl/:
    permalink: /nl/{slug}/
    template: index-nl
    filter: 'tag:hash-nl'
  /es/:
    permalink: /es/{slug}/
    template: index-es
    filter: 'tag:hash-es'

taxonomies:
  tag: /tag/{slug}/

 
```

further you need to label every post and page with a language tage which is in this case #nl, #en, #es. For Dutch, English and Spanish

for more detailed instructions read the following tutorial:
https://ghost.org/tutorials/multi-language-content/





&nbsp;

![screenshot](https://user-images.githubusercontent.com/120485/49328081-0e192680-f59d-11e8-808a-e6d6bcfa8419x.png)


&nbsp;

# First time using a Ghost theme?

Ghost uses a simple templating language called [Handlebars](http://handlebarsjs.com/) for its themes.

We've documented our default theme pretty heavily so that it should be fairly easy to work out what's going on just by reading the code and the comments. Once you feel comfortable with how everything works, we also have full [theme API documentation](https://themes.ghost.org) which explains every possible Handlebars helper and template.

**The main files are:**

- `default.hbs` - The main template file
- `index.hbs` - Used for the English home page
- `index-nl.hbs` - Used for the Dutch home page
- `index-es.hbs` - Used for the Spanish home page
- `post.hbs` - Used for individual posts
- `page.hbs` - Used for individual pages
-
- `tag.hbs` - Used for tag archives
- `author.hbs` - Used for author archives

One neat trick is that you can also create custom one-off templates just by adding the slug of a page to a template file. For example:

- `page-about.hbs` - Custom template for the `/about/` page
- `tag-news.hbs` - Custom template for `/tag/news/` archive
- `author-ali.hbs` - Custom template for `/author/ali/` archive



# Copyright & License

Copyright (c) 2013-2020 [HTML5 UP](https://htmlup.net) & [Ghost Foundation](https://ghost.org) - This theme is licensed under both the [MIT and Creative Commons Attribution 3.0](LICENSE). Please note that the terms of the Creative Commons license require that you maintain the footer attribution to freely use this theme.
