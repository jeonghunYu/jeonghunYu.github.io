---
layout: post
title: Create a blog using devlopr jekyll
author: Sujay Kundu
date: '2017-11-19 14:35:23 +0530'
category: guides
tag: 
    - jekyll
    - blogging
summary: Getting Started - Build your blog using devlopr jekyll
thumbnail: /assets/img/posts/devlopr.png
---

If you are a developer, who want a fast static website with no cost for hosting/domain stuff. This guide will help you setup a blog for you. The blog files resides in your github repo and the site is build with any of the free deployment providers of your choice such as [Github Pages](https://pages.github.com) / [Netlify](https://netlify.com) / [Heroku](https://heroku.com). You can also connect your custom domain later with SSL enabled :D !

#### Using [devlopr starter](https://github.com/sujaykundu777/devlopr-starter) Template.

##### **Step 1** - Create a new repo for your blog in [Github](https://github.com)

Go to [devlopr starter](https://github.com/sujaykundu777/devlopr-starter). Click on the "Green" - **Use this Template** Button.

![devlopr starter template](/assets/img/posts/devlopr-starter.png){:class="img-fluid"}

Create a new repo with name as "**yourusername.github.io**" replacing yourusername with your github username. 

 ![devlopr starter template](/assets/img/posts/1.png){:class="img-fluid"}


**Note :**
You can use any other name like "my-blog" but then , if you are using github pages for deployment. your site will be built at the subdomain - yourusername.github.io/my-blog. 

 

##### **Step 2** - Create a new branch "gh-pages" 

From the master branch create a new branch "gh-pages". This we need to host our changes in our blog. The built site is automatically deployed to **master** branch 

![devlopr starter template](/assets/img/posts/2.png){:class="img-fluid"}

##### **Step 3** - Clone your repo locally 

You will get the clone url from here: 

![devlopr starter template](/assets/img/posts/3.png){:class="img-fluid"}

`git clone https://github.com/yourusername/yourusername.github.io.git`

##### **Step 4** - Checkout gh-pages branch locally

move to your project directory 
`cd yourusername.github.io`
checkout gh-pages branch 
`git checkout gh-pages` 
open the directory using vscode
`code .` 

##### **Step 5** - Make all your changes in gh-pages branch. 

Open the files using VSCode and edit **_config.yml** and edit with your details:

![devlopr starter template](/assets/img/posts/4.png){:class="img-fluid"}

We will be using our **gh-pages** branch to make changes to our blog (deployment branch). The site will be built on the **master** branch (site will be served from here).

- **_config.yml** file - replace with your own details 
- **_posts** - Add your blog posts here 
- **_includes** - You can replace the contents of the files with your data. (contains widgets)
- **_assets/img** - Add all your images here


##### **Step 6** - Install Ruby 

We need [ruby](https://www.ruby-lang.org/) to build our site locally. You can check out this [Guide](https://www.ruby-lang.org/en/downloads/) to install the same for your OS. 

After installation check if its working:

```
ruby -v
ruby 2.5.1p57 (2018-03-29 revision 63029) [x86_64-linux-gnu]
```

##### **Step 7** - Install Bundler 

`gem install bundler`

After installation check if its working:

```
bundler -v
Bundler version 2.0.1
```

##### **Step 8** - Install the dependencies 

`bundle install`

##### **Step 9** - Serve the site locally (development mode)

`bundle exec jekyll serve`

![devlopr starter template](/assets/img/posts/5.png){:class="img-fluid"}

You can visit the site at http://localhost:4000


![devlopr starter template](/assets/img/posts/6.png){:class="img-fluid"}

Now you can make your changes to your blog locally,


#### For how to configure your blog and add posts. You can refer to this [Article (coming soon)](#)

 After you think its fine, proceed with the next step !


##### **Step 10** - Making it Live (Deploy your Blog)

After you are happy with your blog. It's time to show it to the world. There are several ways which are possible for deploying the blog for free. Below is the list of build guides :

- [Deploy your blog using Github Pages and Travis CI](#)

- [Deploy your blog using Netlify Hosting and Netlify CMS (Coming Soon)](#)  


