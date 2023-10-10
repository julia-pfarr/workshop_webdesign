Material for Mkdocs has a lot to offer in terms of making your website pretty and adding useful features. 

## Adding a pdf file

To display your CV you might want to have a pdf file added on your website instead of formatting your CV in Markdown. Here's how:



##### Task 1



## More extras

##### Task 2

Add all the markdown extensions to your `mkdocs.yml` file, like so:
```yaml
markdown_extensions:
  - admonition
  - abbr
  - attr_list
  - def_list
  - footnotes
  - meta
  - md_in_html
  - codehilite
  - pymdownx.critic
  - pymdownx.caret
  - pymdownx.keys
  - pymdownx.mark
  - pymdownx.tilde
  - pymdownx.tabbed
  - pymdownx.details
  - pymdownx.inlinehilite
  - pymdownx.smartsymbols
  - pymdownx.tasklist:
      custom_checkbox: true
  - pymdownx.superfences
  - pymdownx.tabbed:
      alternate_style: true
```

##### Task 3

Go to the website of [Material for Mkdocs] and add some nice features to your website. 

Here's a short overview what you can do:

!!! note "With a title"

    Note with a title

!!! info inline end ""

    Notes on the side

!!! note ""

    Note without a title

**Extra task:** Try make your own icon for admonitions!

<br><br>

You can make annotations (1) to your text. Even with emojis (**Extra task**)
{ .annotate }

1. I'm an annotation! I can contain `code`, __formatted
    text__, images, ... basically anything that can be expressed in Markdown.

[You can make a button](#){ .md-button .md-button--primary }    

```
Code blocks
```

| Table     | table                     |
| ----------- | ------------------------------------ |
| `Table`       | table  |


Footnotes[^1]. 

Highlighting:

- ==This was marked==
- ^^This was inserted^^
- ~~This was deleted~~

**...and much more! Try everything out!**


## Blog

If you want to set up a blog on your website you might want to think about using the [Blog-Plugin] by Mkdocs. This plugin enables features such as adding a date, reading time, tags, and topics for your blog entries ([example Blog] from their website). If you don't use the Blog-Plugin you can just as well create usual Markdown-files and order them in your .yaml file accordingly, like so:
```yaml
nav:
- Home: index.md
- About: about.md
- CV: cv.md
- 'Blog':
  - Topic 1: Topic1.md
  - Topic 2: Topic2.md
  - Topic 3: Topic3.md
  - ...
```

However, this will become a bit chaotic and unclear over time, depending on how many blog entries you want to make. Thus, I recommend looking into the Blog-Plugin to make your blog look more professional. 




[Material for Mkdocs]: https://squidfunk.github.io/mkdocs-material/reference/
[^1]: I am a footnote.
[example Blog]: https://squidfunk.github.io/mkdocs-material/blog/
[Blog-Plugin]: https://squidfunk.github.io/mkdocs-material/plugins/blog/