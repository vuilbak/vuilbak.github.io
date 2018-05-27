# vuilbak jekyll website

## Structure

The website revolves around its homepage, for which the structure is mainly
specified in `_layouts/home.html`. This homepage is populated by (1) blog posts,
(2) links to other pages in the vuilbak ecosystem and (3) boring or
pseudo-boring pages (the classic 'about's and 'contact's and what have you).

*Blog posts* - live in the `_posts` directory and are written in markdown
syntax, allowing everybody to write a basic piece and publish it without the
need to mess in html and css to make it look decent. For a reference to
markdown, see https://daringfireball.net/projects/markdown/.

*Other pages* - this is the heart of the vuilbak website, the accumulation of
random insignificant pages which live their own lives. These sites are variably
maintained, neglected, removed, replaced, broken, fixed and hidden. These sites
live in dedicated subdirectories of the `pages` directory. The homepage is
automatically populated with links to these pages by reading information from
the `home.yaml` data file in the `_data` directory. This file looks like this
(an excerpt):

```
column_2:

  - url: pages/clouds/
    img: cloud.png
    width: 100px
    bg: "#b6fbfb"
```

This specifies to include a link to the `clouds` page, with an image
`cloud.png` found in `assets/img/`, wit a width of 100 pixels and a background
color which is some kind of pale super lame blueish color (`"#b6fbfb"`).
Using this approach, a new page is easily entered in the vuilbak whole by
writing an analogous entry as the above pointing to the relevant files.

*Extra pages* - these are also specified in markdown documents which are
inserted in the `pages` directory. The main purpose of these files is to allow
a place on the home page for simple text based pages that are not posts. For
example an about or contact section, but also a pamphlet, love letter, terms of
agreement list *etc.*

## Styles

Currently, mainly `w3.css` and the basic minima theme from jekyll are used.
Custom css classes are defined in `_sass/vuilbak/_base.scss`. This css
stylesheet is loaded last so it overrides possible previously defined stuff.
