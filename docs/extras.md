Material for Mkdocs has a lot to offer in terms of making your website pretty and adding useful features. 

## Adding a pdf file

To display your CV you might want to have a pdf file added on your website instead of formatting your CV in Markdown, like this:

<object data="../artifacts/example.pdf" type="application/pdf" height= "500" width="100%">
</object>

##### Task 1

Create a new folder inside your `docs` folder called `artifacts`. Place your pdf-file inside the `artifacts` folder.

##### Task 2

Open your `CV.md` file. Place the following html-code inside the file:
```html
<object data="../artifacts/Filename.pdf" type="application/pdf" height= "500" width="100%">
</object>
```
You can adjust the height and width as you wish. 


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

1.  I'm an annotation! I can contain `code`, __formatted
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

##### Task 4

Go to the [setup page] by Material for Mkdocs and find out about more customizations. E.g., for the footer Icons for social media can be included by defining them in the `mkdocs.yml` file like this:
```yaml
extra:
  social:
    - icon: fontawesome/brands/twitter
      link: https://twitter.com/your-account
    - icon: material/email
      link: mailto:email-address
```
The icon will then appear in the footer of your website. You can search for the icons [here], replacing the `-` with `/` when you enter it in your yaml-file. 


## Blog

If you want to set up a blog on your website you might want to think about using the [Blog-Plugin] by Mkdocs. This plugin enables features such as adding a date, reading time, tags, and topics for your blog entries ([example Blog] from their website). 

If you don't use the Blog-Plugin you can just as well create usual Markdown-files and order them in your .yaml file accordingly, like so:
```yaml
nav:
- Home: index.md
- About: about.md
- CV: cv.md
- Blog:
  - Topic 1: Topic1.md
  - Topic 2: Topic2.md
  - Topic 3: Topic3.md
  - ...
```

However, this will become a bit chaotic and unclear over time, depending on how many blog entries you want to make. Thus, I recommend looking into the Blog-Plugin to make your blog look more professional. 

## License

You should think about adding a [license] to your website. You can either display the license as an [extra tab] or include it in the copyright section, like so:
```yaml
site_name: Workshop Web-Design for Scientists
copyright: <a href="https://choosealicense.com/licenses/mit/">License</a>
  &copy; 2023 Julia-Katharina Pfarr<br>
``` 

## Imprint

In the same way you can add a license to your copyright footer, you could add an imprint. This is **not necessary** for a non-commercial personal website but only for commercial websites. 

## Privacy Policy

If you set up your website in a way that you collect private data (e.g., newsletter or blog subscriptions), you will need a [Privacy Policy]. You can include this in the copyright footer as well, just as the license above. 

[Material for Mkdocs]: https://squidfunk.github.io/mkdocs-material/reference/
[^1]: I am a footnote.
[setup page]: https://squidfunk.github.io/mkdocs-material/setup/
[example Blog]: https://squidfunk.github.io/mkdocs-material/blog/
[Blog-Plugin]: https://squidfunk.github.io/mkdocs-material/plugins/blog/
[license]: https://creativecommons.org/
[extra tab]: https://squidfunk.github.io/mkdocs-material/license/
[Privacy Policy]: https://www.termsfeed.com/blog/privacy-policy-personal-websites/