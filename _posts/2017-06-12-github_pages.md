---
excerpt: "Check why I did this, what restrictions do I face now and how you can move to GitHub Pages."
header:
  overlay_color: "#333"
  overlay_filter: 0.5

title: I have moved to GitHub Pages
date: "2017-06-12 16:00:00"
categories: lifestyle
---
GitHub Pages is a free hosting service. Each project on GitHub can have its website. What's even better — you can attach a custom domain or use Github's https subdomain.

## Motivations

Previously this blog was hosted on my own VPS Ubuntu server. It was great at the beginning. Configuration and all that stuff weren't so difficult as I firstly though. Possibilities of that approach were limitless and sometimes I was uploading my games or do other experiments on that server. All fun. Then I decided that each service I'm working on should have a separated server. So I did. Finally, it was a really good decision but now I have multiple servers and multiple responsibilities. Few month ago my private cloud server broke — something with Linux kernel or server's HDD. Rather, service provider's error than mine because the server was working great for more than a year. The thing is, I had troubles because all my files needed to be moved elsewhere. I began to consider — what if my blog's server will break? Do I have backups? Yep. Do I want to lose half of day (yeah half...) just to restore things as it should be? Nope! 


Here comes GitHub Pages. Simple solution. You have static Markdown files which are converted to blog posts. **No database, no server, no safety threats, no costs!** All you need is ~~love~~ git repository!


Posts can be written in Markdown or HTML. All post files must begin with _YAML Front Matter_ which is simply key: value list of properties. It looks like this:
```
---
title: I've moved to GitHub Pages
date: 2017-06-12 16:00:00
categories: lifestyle
---
```
In this _YAML Front Matter_ header, you can specify things like header image, post title, description, date, layout, categories and much more. Search in the _Jekyll's_ documentation for more info.


Another great thing is a migration of your current blog to GitHub Pages. You can easily migrate here from Wordpress, Ghost.js, Joomla, and others.

## Restrictions

These are static files. No server-side code can be running here. So if you are using your current blog server to run some scripts or other services it cannot be done here.

No GitLFS support — as I know not many people using LFS (large file storage) but I do. Repository for the video blog or the photo blog will increase drastically with every change of binary files. You can host binaries elsewhere and embed them to your Pages blog but host this here is a poor idea.

For custom domains, there is no out-of-the-box SSL solution.

Not all _Jekyll_ plugins can be used on GitHub Pages. There is a list of allowed ones. So if you already have a blog running on _Jekyll_ be sure that plugins you are using aren't necessary anymore. This limitation has security impact because there is no risk to run some malicious code from custom plugins.


## Instructions

The first configuration and using is rather straight forward. I'm not familiar with Ruby hence it took me few hours to understand the idea behind _Jekyll_.

The best solution for me was first creating an empty website with `index.html` on it. Ensure that this works and then start over again. Then I've found a great _Jekyll_ theme called _Minimal Mistakes_ and do as they said in instructions. After a while, I understood where are config files, what to change and how to adjust theme for my needs.

There is plenty of ready to use themes. Many are of poor quality but some (as this I use) look really professional. Great thing is that you can customize all as you need. All CSS code and layouts are open so you can change as you wish.

I will not repeat online resources. I encourage you to make similar way as mine described above. On the bottom of this blog post, you can find useful links.

## Ready to go

To sum it up. This is my beginning with GitHub Pages. If I will find some pros or cons I will definitely update this post and notify you by Twitter. For now, it looks like a perfect solution for blog or product page.

## Resources

* [GitHub Pages](https://pages.github.com/)
* [Jekyll official page](https://jekyllrb.com)
* [Jonathan McGlone guide for GitHub Pages beginners](http://jmcglone.com/guides/github-pages/)
* [Jekyll import tools](http://import.jekyllrb.com/)
* [Jekyll plugins on GitHub Pages site](https://help.github.com/articles/adding-jekyll-plugins-to-a-github-pages-site/)
* [Minimal mistakes theme](https://mmistakes.github.io/minimal-mistakes/)