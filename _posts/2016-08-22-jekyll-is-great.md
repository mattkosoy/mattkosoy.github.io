---
layout:     post
title:      Using the Jekyll for the website.
date:       2016-08-22 00:00:00
summary:    My take on how to get started with Jekyll.
---

## TL;DR: 
* <a href="https://git-scm.com/">Git</a> for all of the things, especially deployment.
* <a href="https://jekyllrb.com/">Jekyll</a> is great. 

## Okay then

<a href="/process/2016/07/20/hecka-tight-method-for-doing-web-development/">I helped my buddy <a href="https://tonyvoorhees.github.io/">Tony</a> got a whole bunch of softwares installed that will make it easy for us to do web development.</a> We customized the look of our CLI, and added some aliases to our environment that will help us save time. Now we can  install a <a href="https://davidwalsh.name/introduction-static-site-generators">static site generator</a>, and then start to create content. I would get into the specifics of what a static site generator is, but many other people have done so already. Therefore I will simply offer some details into Tony's specific scenario.

Tony, like a lot of designers, was using Wordpress as a content management system. Back in the day this worked really well because Wordpress is very easy to install and configure. The problem with Wordpress is because it is so popular it has become a target for hackers and spammers. The extra overhead that is involved in managing a Wordpress site has become a major pain point for many people. He had done some prototyping of his site in static HTML. He had asked me how he could integrate this into an app that stores the content into a database. 

## Doctor Jekyll and Mister Github Pages

I suggested to Tony that he install <a href="https://jekyllrb.com">Jekyll</a>. If he did this then he wouldn't need to use a database because Jekyll would simply serve up the HTML that he has already created. 

    gem install jekyll
    cd PATHTOTONYSPROJECT
    jekyll serve

Then I had Tony open up `http://localhost:4000` in his web browser, and voila the static markup that he had been prototyping appeared as expected. This enabled Tony to take his website from concept to completion. The last step for Tony was to publish his site, and the way to do that was by using <a href="https://git-scm.com/">Git</a> and <a href="https://pages.github.com/">Github pages</a>. 

## Deploy to the cloud!

Publishing  work to github pages is easy, fast, and free. Working with `git` at first was a bit of a challenge for Tony. What I did to help Tony better understand the workflow was break things down into five steps. He knew that he wanted to use `git` to manage and deploy his stuff but he wasn't quite sure about where to start. I helped by stating that the way to start is at <a href="https://github.com">Github</a> by creating a new public repository called `USERNAME.github.io`. Then on your laptop we can add that new repository as a remote.

We use `git` to track changes to our soruce code. `Github` is a service provider that hosts git repositories. In the context of a static website this source code is our content, mostly markdown and html. There are some other types of files that go into a Jekyll site, but those things are meant to be covered in another post. In the terminal I showed Tony how to navigate to his project folder, and then initialize a new git repository

    cd ~/sites/tony
    git init


Now you are set up to make changes to the site. In Tony's scenario this meant making sure that <a href="http://getbootstrap.com/">Bootstrap</a> was in place, and that his assets were in there. Tony started to add a bunch of changes to this feature branch, and was eager to see his changes on his site. After a bit Tony was ready to publish his work to as a Github page. To do this I helped Tony add the github page repository to his local working copy, and push his changes up. 

    git remote add origin https://github.com/USERNAME/USERNAME.github.io
    git push origin master


The `USERNAME/USERNAME.github.io` bit should correspond to the repository you created earlier. Duh. 

Boom! You should be able to see your site at `https://username.github.io`.

