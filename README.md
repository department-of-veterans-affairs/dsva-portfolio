# dsva-portfolio

This is a portfolio site for the Digital Service at VA team.


## Adding or editing your basic information

If you're new to the team or would like to update your profile information for the site follow these steps:

First create a profile picture and place it in `img/team`. Make sure to name it logical like `harriet_tubman.jpg`. Note that your picture should be 350x150 or similary proportioned to render correctly on the site.

Under the `team.yml` under the `_data` folder. In this document you'll see a list of team members as an array like so:

```
- reference_name: kavi_harshawat
  name: Harriet Tubman
  title: UX Designer and Researcher
  picture: http://placehold.it/350x150
  twitter: htubman
  github: hariettubman
```

If you see yourself there, feel free to edit your personal information otherwise create a new array with the same formatting at the bottom of the list. 


## Creating a project page

We can use this portfolio site to list out the project that the DSVA team is working on. If you'd like to create a new project page follow these steps:

Create a new markdown file and save it under the `_posts` directory with the following filename formatting: `YYYY-MM-DD-example-project.md`. This formatting of the title is important so make sure it follows the pattern!

Once you've created your markdown file, you need to put in what's called "Frontmatter" surrounded by `---` at the top of the page. This Frontmatter contains meta-information about project and how it's webpage should look online. Take a look at the following example:

```
---
layout: post
category: work
permalink: example-project

title: Example Project
subtitle: Appeals Cupcakification
date-updated: 6/12/15
contributors: 
- Kavi Harshawat
- Jeff Maher
- Matthew Weaver
- Emily Wright-Moore
- Alex Gaynor
---
```

As we mentioend above all the Frontmatter is surrounded by `---`. The `layout` variable is what template the page should follow. In this case we should just use the `post` template. We set the `category` to `work` to make it easy to collect all the projects on the work landing page. The `permalink` should be set to whatever you want the URL to looklike in browser's address bar (best to keep this simple). 

A couple of lines below we have variables that are used in the post itself. The `title` should be the title of your project. The `subtitle` variable is used on the work landing page. Use the `date-updated` variable to make let others know when this project was last updated. Finally, you can list out all the `contributors` to a project by listing them out like the example above. This will automatically generate a little grid with these people's faces and details at the bottom of the project page (pretty nifty, eh?). If you list someone here, make sure they're also listed in the `_data/team.yml` file or their information won't show up!

Finally, below the second `---` after the frontmatter, write up the description of your project. You can use markdown syntax, and the content will be formatted appropriately on the site. 

`{{ site.url }}` is a variable for the base-website URL. It's important because it tells the browser where to look for the image. If you'd like to add an image to your description, use the normal markdown syntax `![Cupcakes!]({{ site.url }}/img/cupcakes.jpg)` (make sure to include your image in the `img/`!). 
