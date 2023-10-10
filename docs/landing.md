The landing page is the first page people see when they visit your website. As your primary goal with a personal website is to introduce *yourself*, my recommendation for a landing page is the following:

- display a welcome-statement to welcome the visitors on your website
- put a picture of yourself, preferably in the center of the landing page
- show your contact information in form of icons 
- name a few buzz-words which describe yourself and your skills best
- link to the most important section on your website

#### Using Markdown 

Surely, you can just apply your newly acquired Markdown-skills to create a landing page. 

##### Task 1

Design your landing page containing the content mentioned above using the resources of mkdocs:

- Format your text in Markdown syntax
- [Images]
- [Buttons] for social media and contact in your `index.md` file. 
- Icons for social media can be included in the Footer of the website as well, by defining them in the `mkdocs.yml` file like this:
```yaml
extra:
  social:
    - icon: fontawesome/brands/twitter
      link: https://twitter.com/your-account
    - icon: ...
      link: ...
```
The icon will then appear in the footer of your website. You can search for the icons [here], replacing the `-` with `/` when you enter it in your yaml-file. 

#### Optional: Using HTML configurations

A more advanced way to create a landing page is using html to override the basic theme configurations provided by mkdocs. This enables you to set not only a customized background color or image but basically everything you would want to change, re-size, add etc. This is a lot more work, though. 

With the following tasks, you can create a landing page looking similar to this:

![landing](assets/images/example_landing.png)

##### Optional Task 1

Create a new directory on the same level as the `docs` folder called `material` and again in this folder a new folder called `overrides`, like this:
```
.
├── docs
├── material
│   └── overrides
└── mkdocs.yml
```

##### Optional Task 2

Create a `home.html` in your `overrides` directory and put the following content:
```html
  {% extends "main.html" %}
    {% block tabs %}
        {{ super() }}

    <!--/* Add library for social media buttons */ -->  
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">    
    
    <style>
    body 
    /* Use "linear-gradient" if you want to add a darken background effect to the image. This will make the text easier to read */
    {background-image: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url('../assets/images/landing.png'); 
    
    /* If you want a background color instead of an image: 
    background-color:powderblue;*/

    /* Position and center the image to scale nicely on all screens */
    background-position: center;
    background-repeat: no-repeat;
    background-attachment: fixed; 
    background-size: cover;

    /* Place text in the middle of the image */
    text-align: center;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    color: white;}

    /* Fixate page */
    .md-header{position:initial}
    .md-main__inner{margin:0}
    .md-content{display:none}@media screen and (min-width:60em){.md-sidebar--secondary{display:none}}@media screen and (min-width:76.25em){.md-sidebar--primary{display:none}}
    </style>

    <!--/* Start content */-->
        <div>
            
            <!--/* Use attributes to define color, size, and alignment of your text; for ALL of the text, not just the header */-->
            <header style="color:white; font-size:50px;"> My header</header>
            <h1 style="color:white; font-size:30px;">Smaller heading</h1> 
            <h2 style="color:white; font-size:20px;">Even smaller heading</h2> 
            <p><br/>This is a very small text without resizing</p>
            <p>This is a reference to another website within a text: <a href="url to website">Name</a></p>

            <!--If you want to put an image:
            <img src="img_girl.jpg" alt="Girl in a jacket" style="width:500px;height:600px;">-->
            
            <!--/* This is a button */-->
            <button onclick="link;" type="button" padding="10px" style="background:white; color: black;" >Get started</button>

            <p><br/><br/><small>This is a suuuuper small text</p></small> 

            <!--/* Use social media buttons; don't forget to size and color the button */-->
            <a href="https://twitter.com/jk_pfarr" class="fa fa-twitter"></a>

        </div>
  {% endblock %}
  {% block content %}{% endblock %}
  {% block footer %}{% endblock %}        
```

**Please see this [HTML info page] for formatting in html language.**

##### Optional Task 3

Create another file in the same directory called `main.html` with the following content:
```html
  {% extends "base.html" %}
```

##### Optional Task 4

Open your `index.md` file and put the following content:
```md
---
template: overrides/home.html
---
```

You should now see your landing page. 

[Images]: https://squidfunk.github.io/mkdocs-material/reference/images/
[Buttons]: https://squidfunk.github.io/mkdocs-material/reference/buttons/
[here]: https://squidfunk.github.io/mkdocs-material/reference/icons-emojis/
[HTML info page]: https://www.w3schools.com/html/default.asp

