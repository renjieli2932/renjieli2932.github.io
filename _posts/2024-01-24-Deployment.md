---
title: My First Post
date: 2024-01-24 16:10:00 +/-TTTT
categories: [Tech]
tags: [ruby, jekyll]     # TAG names should always be lowercase
---

Hey there, this is the first post on Renjie's personal blog.

Here I will briefly recap how I built it. Yeah I followed bunches of tutorials online and I think you can also easily find them, or you can follow this post lol. 

## 1. Installation of Ruby

I don't think it is necessary cuz you can directly fork [Chirpy](https://github.com/cotes2020/jekyll-theme-chirpy/fork) theme to your GitHub Pages and make modifications based on that. 

But if you want to have a preview of how the post looks like without relentlessly commit & push , just configure it , locally.

*I'm not sure if every step can also be applied to devices running Windows, no validation has been made.*

I know nothing about (ch)ruby and I guess this is something like conda which allows me to install different versions of Ruby. I basically followed the [official tutorials](https://jekyllrb.com/docs/installation/) of jekyll. 

I am using MacBook and I found no issues following the tutorial. But you **don't** need to execute the **final** step :

```bash
gem install jekyll
```

cuz you can easily install every essential packages via chirpy starter.

> Just make sure after typing 
```bash
ruby -v
```
in terminal , the ruby version shown on the screen is the version that you specified. If it is still ruby 2.x(pre-built in MacOS), you may have missed some steps in the tutorials. 
{: .prompt-tip }


## 2. Fork Chirpy starter to your own GitHub Pages

Simply follow the official [README](https://github.com/cotes2020/chirpy-starter) to fork the chirpy starter to your GitHub Pages.

Before cloning it to local, type 'YOURUSERNAME.github.io' to have a brief preview. Yeah you are 50% finished. 

Clone the repo to local and compile it. 

Wait patiently and the chirpy theme will be automatically deployed to your local machine. 

You may have the local access <http://127.0.0.1:4000> to your blog after you execute

```bash
jekyll -s
```

Then modify the _config.yml, add your first post (like this post), commit & push, now you have your post on GitHub Pages. Congratulations!


## 3. Custom domain name

If you have a custom domain name and you want to link it to GitHub Pages, you need to :

- Create a file named CNAME in your root directory, add the domain name.

> DO NOT add any prefixes like **https://** , just the custom domain name like **CUSTOMNAME.YOURDOMAINNAME.com**
{: .prompt-tip }

- In your domain website, add a DNS nameserver. For example, type: 'CNAME', name: 'CUSTOMNAME', data: 'YOURGITHUBUSERNAME.github.io'

- In your github repo, select 'Settings - Pages', then type your domain name as well. Scroll down, type the full name of the custom domain, like 'CUSTOMNAME.YOURDOMAINNAME.com', then save. 

Wait for a while, now you can access your GitHub pages using your own domain name.

