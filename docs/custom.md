## Getting started

Open your terminal and type: 
```
mkdocs new . 
```
This creates template files for the website in your current directory. Your folder now contains the following:
```
.
├── docs/
│   └── index.md
└── mkdocs.yml
```

##### The docs folder

Over the course of this workshop we will heavily populate the docs folder with different kind of files. All the content you want to display on your website in form of text or images will live in this folder. Most of the time, this content is written with Markdown which enables you to do nice formatting, include code-chunks, images, tables etc. etc.

##### The YAML-file

The mkdocs.yml file determines the settings of your website. In this file you state in which order you want your content (navigation), which theme, color, font, language; change icons and copyright etc. etc. 

**Find more background information on Markdown and YAML in the [Google Slides].**

After you created the template folder you can already check how the template website looks by creating a localhost address. For this, you simply have to type the following command in the terminal (inside your website directory): 
```
mkdocs serve
```
Copy the [localhost:8000] into a browser tab. You can now see how the template website looks like: 

![](assets/images/creating-your-site.png)


It will always automatically update as soon as you change something in your configurations (i.e., the YAML file) or your content (i.e., in your Markdown files). 

## First Customizations

As mentioned above, you can customize your website regarding a lot of features. The documentation of mkdocs-material is very comprehensive and easily understandable, which is why I will link to their site for many of the instructions. 

##### Task 1

Open the mkdocs.yml file: 

- Give your website a name 
- add the theme of the design you're using (here: material)
- hint to the directory where all your Markdown files and other content will live
    ```yaml
    site_name: example      
    theme:                  ##under theme goes everything design related
        name: material      
    docs_dir: docs            
    ```

##### Task 2

Please visit the mkdocs-material [setup page] and go through the first four configurations: 

- colors 
- fonts 
- language 
- logo and icons

Changes are made in the YAML file under `theme:` and apply immediately. You can check the changes on the website in your browser via the localhost address.

!!! note "Best Practice"

    Create a new folder in the *docs* directory called *assets* and within assets a new directory called *images*. In this images folder you should store all the images you'll use on your website. 
    ```
    .
    ├── docs
    │   ├── assets
    │   │   └── images
    │   │       ├── creating-your-site.png
    └── mkdocs.yml
    ```

## Filling your website with content

Content divided in different sections is created by multiple Markdown-files. For each section you need a new Markdown-file. In this file you write and format the text (and images, code, citations etc.) according to the Markdown syntax.  

##### Task 3

- Make yourself familiar with the [Markdown syntax]
- Create new .md files and fill them with content, e.g., 
    - a section to introduce yourself in a section (e.g, "About")
    - a section where you outline your research interests and display some related figures 
    - a section with contact details 
    - a Blog section
    - etc. 

???+ note "Landing page"

    How to create a pretty landing page is outlined in another section. Please focus on the content in this task, only. 

???+ note "Curriculum Vitae"

    Instead of displaying your CV using .md you can also import a pdf-version of your CV. If you'd like to do so, please see the section "Pretty and Useful Extras". 

## Setting up the navigation

Now that you gathered the content for your website you will need to determine the order and the look of your navigation bar. 

##### Task 4

Open your .yml file and define the order of your content, e.g.:
```yaml
    site_name: example
    theme:
        name: material
    docs_dir: docs   
    nav:
        - Home: index.md ##this is fixed! The .md file of the landing page needs to be named "index.md"
        - About: about.md
        - Research interest: interest.md
        - Contact: contact.md
        - ##etc
```

##### Task 5

Read through the [navigation configurations], choose the ones you like and apply them to your website by defining it in your .yml file. For example, the navigation (and other) setups for this website look like this:
```yaml
site_name: Workshop Web-Design for Scientists
theme:
  name: material
  palette:
    primary: blue grey
  font: 
    text: Montserrat
    code: Roboto Mono  
  language: en
  logo: assets/images/nowa-white.png
  features:
    - navigation.tabs           #navigation tabs vertically aligned under on the top
    - navigation.tabs.sticky    #tabs stay visible when scrolling down
    - navigation.top            #back-to-top button 
    - navigation.sections       #sections (=.md files) rendered
    - navigation.expand         #left sidebar will expand all collapsible subsections 
    - toc.integrate             #"Table of contents" is not separately shown on the right but integrated in the navigation on the left 
```


[Google Slides]: https://docs.google.com/presentation/d/16Rgdn_-uqjZVwmeyDhGL41vKMRCFA0dSom2IpreZ59I/edit?usp=sharing
[setup page]: https://squidfunk.github.io/mkdocs-material/setup/
[localhost:8000]:http://localhost:8000
[Markdown syntax]: https://www.markdownguide.org/cheat-sheet/
[navigation configurations]: https://squidfunk.github.io/mkdocs-material/setup/setting-up-navigation/