---
title: How to Build a Blog for FREE - Setting up Jekyll (Part 2 of 3)
subtitle: This article walk you through a simple way of setting up a Jekyll blog for free. Jekyll is a static site generator which lets you build static site on Github pages.
header-img: Jekyll free blog.webp
categories:
  - blogging
featured-image: Jekyll free blog.webp
slug: build-blog-for-free-part-two-jekyll
excerpt: This is the part 2 of series "how to build a blog for free". In this part, I will walk you through step-by-step process of installing Jekyll and build a blog website for free. 
toc: true


---

So you finally decided to build a blog that costs you nothing. I am sure you have read <a href="https://rakshitsoral.ga/blogging/2019/10/18/build-blog-for-free-part-one/">“Part 1”</a> of this series, which helps you to take the decision. Buckle up, as I take you through the next part which deals with building a free blog with Jekyll on Github pages. 

To make you navigate through the blog in an easy way, I divided this blog into two parts:

<ul class="round">
<li>Choosing the platform: Why Static Site Generator? What are its advantages over Wordpress?</li>
<li>Jekyll: Getting Started with Jekyll in Ubuntu and Windows</li>
</ul>

## Choosing the platform: Why Static Site Generator?

### Personal Anecdote

In 2017, I created my <a href="https://huntfordigital.com/" target="_blank">first ever blog</a> on WordPress and it was an awesome experience. The process was not at all time consuming, let alone cost-effective. Since a lot of marketing experiments deal with Wordpress, it was obvious to be my initial choice. However, I wanted to experiment with something different; something which makes me learn one thing or two. 

I stopped working on Wordpress as I invested a major chunk of my time learning HTML, CSS, and Javascript. SEO was not new to me; I am doing it since the beginning of my career. I wanted to do something more interesting.

In 2019, I decided to build my personal site on Github. I played around with Bootstrap for a while but found it time-consuming. The other day a friend of mine mentioned the concept of static-site-generators to me, I found it appealing. Since my favorite note-taking format remained Markdown, I liked the concept at first glance.

Wordpress was always an alternative for me but I dislikened the whole process of choosing, buying and renewing the hosting and domain name. With Static-site-generators, I had the option of serving the HTML on Github pages for FREE. Here’s why I settled on Jekyll using Github pages after trying out several Static-site options such as Pelican and Hugo. Of course, I had my other reasons to support the decision such as speed, cost-savings, security, maintainability, and customizations. 

Let’s take these advantages one-by-one:


### Cost

One of the main reasons for choosing Jekyll over Wordpress would be the cost. 

Wordpress makes your pocket loaded with investments like domain name, hosting (webserver), PHP and a database. Although most hosting plans give you a good deal for the first year but after a couple of years, it does get pricey. 

For me, since I have hosting and domain for about three years, this came out to Rs. 2500 (hosting for 3 years) + Rs. 1000 (domain for 1 year). With static sites such as Jekyll, the cost goes down to Rs. 0/year (or only Rs. 1000 if I want a .com domain extension). What’s more, you can host your static site for free using platforms like Github Pages and Netlify. 

### Speed

Another solid reason to build a blog with a Static-site generator is speed. 

Wordpress gives you a dynamic way of loading the content live in a database, which gets converted into HTML only when a user wants to see the page. The entire process is request-heavy with steps like building the page from a template or theme, grabbing the content and sending the completed page to the user. 

With Jekyll or any other static site, the whole site gets uploaded to the server as a folder full of assets (HTML, CSS, images, etc.). The entire process of requesting and fetching the content is seamless as the assets are already statically loaded on the server. This improves the page load speed significantly. With Wordpress, however, you still need to optimize the performance and speed with a variety of plugins which slows down the website. If you are still not convinced, Nikola has written a nice blog on the topic: <a href="https://getnikola.com/handbook.html#why-static" target="_blank">“Why Static?”</a>.

Below are tests I ran using the <a href="https://tools.pingdom.com/" target="_blank">Pingdom Website Speed Test</a> on my WordPress and static site.

#### WordPress Test

![Wordpress test](/images/Wordpress speed test.webp)


#### Static Site Test

![Wordpress test](/images/static site speed test.webp)


### Security

When was the last time you heard someone telling you to update your CMS and plugins for better security in Wordpress? If the stats are to be believed, over <a href="https://www.wpwhitesecurity.com/statistics-70-percent-wordpress-installations-vulnerable/" target="_blank">70% of all WordPress installs are vulnerable to known security glitches.</a>

Static sites, on the other hand, give you a free hand to experiment with your code without having to worry about malware. Static sites are built on a production machine (probably the machine you are reading this on) by static site generators, which take your code and spit out flat HTML files with CSS and JavaScript. When a user requests a page from your site, the server just sends them the file for that page, instead of building that page from various assets each time. No build process means standard hacking attacks like scripting or database security exploits just don’t work.

## Choosing Jekyll as a static site generator: Getting Started 

The other day I was looking for options to build a static-site, the numbers are overwhelming. At the time of writing this blog, there are over 463 options to build a static site. And the numbers are increasing day by day!

Remember I mentioned about trying options such as Pelican and Hugo for building a blog. It was fun playing with them but I decided to stick with Jekyll. I will tell you exactly the reasons for choosing Jekyll as a static site generator in an upcoming blog. 

### Prerequisite of working with Jekyll

Although you won’t require much language knowledge to get a static site up and running, I would still recommend you to polish basic HTML and CSS skills. You will require them during website customization. As an addition, I would recommend you to learn basic Git commands to work on Ubuntu. 

Now that the prerequisites are known, let’s move on and learn how to build a blogging website with Jekyll for Free. 

## Building a FREE blog: Setting up Jekyll on Github Pages

<h3><b>#Step 1:</b> Installing Jekyll with Ruby</h3>
 
<b>First things first, let's install Jekyll on your computer</b>

Since Jekyll is a static site generator, there is no involvement of the server, database, and backend. All you need is to have a local copy of the site on your computer. You will edit the local files on your machine directly and deploy the changes to the Github repo which is the online version of the site. 

To work with the local copy, you need to install Jekyll on your computer. The first step would be to update all the system packages in Ubuntu to their latest release. 

<pre>sudo apt update
sudo apt -y upgrade
sudo reboot</pre>

To work with Jekyll, you will need to have a working Ruby development environment which includes libraries. Use the following commands to install Jekyll and various build tools required:

<pre>sudo apt -y install make build-essential</pre>

<b>Install Ruby package and development tools:</b>

<pre>sudo apt -y install ruby ruby-dev</pre>

The next step would be to instruct Ruby’s gem package manager to place gems in the user’s home directory.  Add Environment variable to <code>~/.bashrc</code> field.

<pre>echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
echo 'export GEM_HOME=$HOME/gems' >> ~/.bashrc
echo 'export PATH=$HOME/gems/bin:$PATH' >> ~/.bashrc
source ~/.bashrc</pre>

Use gem to Install Jekyll and Bundler which is a tool used to manage gem dependencies. 

<pre><b>$ gem install bundler</b>
Fetching: bundler-2.0.2.gem (100%)
Successfully installed bundler-2.0.2
Parsing documentation for bundler-2.0.2
Installing ri documentation for bundler-2.0.2
Done installing documentation for bundler after 2 seconds
1 gem installed</pre>

Install Jekyll on Ubuntu with the following command:

<pre>$ gem install jekyll</pre>

<h3><b>#Step 2:</b>Choose a Jekyll theme you like to have on your Website</h3>
This is the thing I like about Jekyll: an extensive theming system. With Jekyll, you will find almost dozens of communities that offers community-maintained templates and styles to customize your site’s presentation. 

You can find and preview Jekyll themes on the following galleries:
<ul class="square">
<li><a href="https://jamstackthemes.dev/" target="_blank">jamstackthemes.dev</a></li>
<li><a href="http://jekyllthemes.org/" target="_blank">jekyllthemes.org</a></li>
<li><a href="https://jekyllthemes.io/" target="_blank">jekyllthemes.io</a></li>
<li><a href="https://jekyll-themes.com/" target="_blank">Jekyll-themes.com</a></li>
</ul>

To install a theme, navigate to the theme’s Github Repo and fork it. In my case, I used Urban Jekyll template on my Jekyll website. Here’s a fork for the same:

![Forking the repo](/images/Forking the repo.webp)


The next step will be to rename the repository to username.github.io. In my case, I shall rename it to rakshitsoral.github.io.

![Renaming the forked repo](/images/Renaming the forked repo.webp)


Now clone the repo to your local machine:

<pre>$ git clone https://github.com/rakshitsoral/urban-jekyll-template.git</pre>

Now move to the folder containing all the files: 

<pre>$ cd urban-jekyll-template</pre>

Initialize the git repo

<pre>$ git init </pre>

Run the site on your local machine:

<pre>$ bundle exec jekyll serve</pre>

Navigate to <a href="http://localhost:4000/" target="_blank">http://localhost:4000/</a> and Voilla, your site is live. It should look like the following image:

![Urban Jekyll Template](/images/urban jekyll template.webp)

It doesn’t look bad, does it? 

<h2 class="note">Wrapping up</h2>
There you go! In this part, you learned how to build a FREE blog using Jekyll. In the next part of the series, I would walk you through the way I customized the whole site. It will include modifying the home page, setting up the Goodreads quote widget, adding recent posts widget and a lot more. 

Untill then, Saayonara!










 











