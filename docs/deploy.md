So far, we only build a local site, meaning that only you can see your website in your browser. To make our website public, we need to deploy it. For this, we are going to use the continuous deployment service of GitHub Pages. You can find background information on what deployment means and continuous deployment on GitHub in these [Google Slides]. 

##### Task 1

If you haven't done already, initialize Git in your local repository:
```bash
cd my-website-folder
git init
```
##### Task 2 

Go to your profile on GitHub and set up a new repository for your website:

- Click on "New"
- Give your repository a name, click "public"(1), and make sure that you **don't** add a README.md (for now)
{ .annotate }

    1.  The repository has to be public, otherwise you can't use the deployment service of GitHub pages.

- Follow the instructions given by GitHub on how to push your local repository to GitHub

##### Task 3

Deploy your website with GitHub Pages.

The developers of Material for Mkdocs wrote a very good documentation about how to deploy your website on GitHub. Thus, I won't add anything to this but redirect you to the section [Publishing your site] on their website. 

[Publishing your site]: https://squidfunk.github.io/mkdocs-material/publishing-your-site/
[Google Slides]: https://docs.google.com/presentation/d/16Rgdn_-uqjZVwmeyDhGL41vKMRCFA0dSom2IpreZ59I/edit?usp=sharing