---
layout: page
title: Creating a new version Specialized.com 
permalink: /projects/specialized-dot-com
summary: Summarizing a year long "prototype to production" effort is hard.
tags: project
page-category: project
image: https://www.dropbox.com/s/s8llpudewqecfci/Screenshot%202016-03-02%2012.25.00.png?dl=1

---


# Here's where the fun begins 

For close to two years I was a Senior Software Developer at <a href="https://www.specialized.com">Specialized Bicycle Components, Inc</a>.  I was a principal engineer and core contributor on the project. My prototypes ultimately became the production application. The team that I was a part of won an (internal company) award for our effort. we were recognized at the spring company meeting in April of 2016.  This is my story of how that site was built.

_[www.specialized.com](https://www.dropbox.com/s/s8llpudewqecfci/Screenshot%202016-03-02%2012.25.00.png?dl=1)_

## A brief history of Specialized.com

By early 2015 it had become painfully clear that <a href="http://www.specialized.com">specialized.com</a> had become obsolete. The experience of interacting with its interface was a little frustrating to say the least. The experience of having to do maintenance work, which was becoming 80% of our job, was also equally as frustrating.

_[It's missing the red Block monster](/images/legacy.specialized.png)_

 I was a member of the webdev team, which is part of the IT department. It was, and still is, their responsibility to create and maintain custom software for Specialized. Specifically: the corporate public facing (B2C) website. This website gets a moderate amount of traffic. It gets approximately 4 million requests per day, on average. Generally speaking the servers were handling about 1000 requests per second, with a 90ms response time. There are a lot of eyeballs on the site at all times.  One of the parts about working on this team that I enjoyed the most was being able to contribute to a project with this much visibility.

The process for deploying code had become very complicated. 
  
> Step 19: don't f*#! it up.

The legacy version of Specialized site was built using JSP files that were included in one another procedureally. There was a huge amount of effort and work and love that went into that creating that version of the site, but the lack of documentation made the change to a new framework inevitable. The appreciation was deep for those team members who had worked long and hard hours on the original site. However everyone knew that techniques had adapted so very rapidly in recent years that the old code had to be abandoned.

On a winters' day in early February our department head called a team meeting. He posed a question to the entire team: What would your requirements be if you wanted to create a new website for specialized?. It was then that the fun began, and after an afternoon of brainstorming we ended up with these 5 core values that the site _had_ to have.
  
1. Responsive UI
2. Hosted on/in the cloud
3. Ease of deployment for dev team
4. Personalized content for the user
5. Localized content for the user

These things are now standard operating procedure for Specialized in production, with the exception of personalized content. That was one feature I was not able to deliver on during my time spent with the company. Four out of five ain't bad.

## Choosing the path forward
  
A vote was taken, and we as group chose to use a full stack Javascript environment. That was, after all, how <a href="http://www.bbc.co.uk/blogs/internet/entries/47a96d23-ae04-444e-808f-678e6809765d">the BBC</a> was doing it. It was good to have that point of reference during our vote. Once we knew that another enterprise was using this type of technology that we could too. By the beginning of March 2015 we had settled in on our new tech stack.

_[we were very productive](/images/prototyping-2.jpg)_

## Making a prototype
  
Because we had a very narrow window to execute with in we wanted to leverage as many off the shelf and open source tools as possible. My contributions at this part were crucial to the success of the project, ultimately. On my own time I did research into current best practices, and I created an app that was based on an <a href="https://github.com/petecoop/generator-express">open source project</a> I found. I also did the following things:

  
* Automate our development processes by using a <a href="http://gulpjs.com/">build system</a>.
* Leverage an <a href="https://expressjs.com/">MVC style</a> architecture.
* <a href="https://heroku.com">Host</a> our application in the cloud for scalability.
* Collect data from our users and store it in a <a href="http://www.salesforce.com/">CRM</a>.
* Do <a href="https://circleci.com/">continuous integration</a> and deployment.
* Sell things online.
* Use tools that enable clear <a href="https://slack.com">communication</a> between team members
* Integrate with a variety of 1st and <a href="https://contentful.com">3rd</a> <a href="https://algolia.com">party</a> <a href="https://greenhouse.io">APIs</a>.
* Adapt our workflow to one that is more agile, and leverages an <a href="https://github.com/thoughtbot/guides/tree/master/protocol/git">open source development protocol</a>.

 Fortunately for me the environment at Specialized, at the time, enabled me to implement all of these things. I worked with team members in multiple departmentsn across the company, and with vendors to help set up this new way of communicating about the website. By the end of April we had delievered a working prototype complete with ecommerce functionality. We won approval from the executive leadership team to begin work on a new site.
 
## Recieving a new content strategy
  
Now that we had a technical direction my team, which is part of the <a href="https://instagram.fsnc1-2.fna.fbcdn.net/t51.2885-15/e35/13696622_998316140266884_948495325_n.jpg?ig_cache_key=MTMwMjI2NTczNzY0NjE1NzE3OA%3D%3D.2">IT department</a>, had to wait for a design to implement.  One of the technical requirements that I was able to put forth was that we utilize an <a href="http://bradfrost.com/blog/post/atomic-web-design/">atomic design</a> method to create a <em>"digital styleguide"</em> of sorts. This ultimately ended up becoming the <a href="/projects/ui-toolkit">UI-Toolkit</a>.  After a while we were presented with an approved content strategy that included these things

1. A homepage with a carousel and calls to action
2. A "Gridwall" page that contains a grid of content blocks, or tiles
3. A "Story" page that included a variety of _Squarespace_ like modules
4. Search with filters and facets
5. A very, very fancy "single page" cart and checkout UI
  
_[A new layout for new times](/images/sbc-mtb.png)_

The visual design and content strategy was done by <a href="http://instrument.com">Instrument</a>.  Their team of designers, developers, and creatives was wonderful to work with. I provided Instrument an instance of an open source software package called <a href="https://fbrctr.github.io/">Fabricator</a> that I thought we could use as a jump off to get things going. For the most part it worked, but not without support from <a href="https://github.com/Instrument/fabricator-assemble">Instrument's dev team</a>.
 
Webdev was not involved with the "core" decision making process that happened with Instrument. Another team from Specialized was, and while that team and the Instrument creatives did their thing Webdev worked on some other projects for about 2 or 3 months. All the while I knew that sooner or later the artwork would be done, and we could get down to the buisness of implementing the vision.  We got our first delivery of things that we could integrate into our fledgling Node app in early September of 2015.

_[@thisisjohnbrown](/images/jb-innout.jpg)_
 
As with any project things twist and turn. During the fall months we spent time researching hosting platforms, and getting some of the more complex internationalization features of the site built.  There's a feature that detects the users IP, geolocates it, and then will request content in a specific locale. We also built a <a href="https://www.specialized.com/change-region">feature</a> that lets the user select whichver region they prefer to be the sourceThere were just about 100 different locales that we provide support for.

Those were some things that we did while Instrument was working on the front end. In early November there was a hand off, and we were able to start implementing <a href="/projects/spceialized-cms/">solutions</a> that enabled the global content team to do their thing with the translations. This was when the structure of the API began to become more consistent with the .yml that lived in the ui-toolkit.


Our effort to get this new version of specialized.com shipped was not going to be stopped by the holiday season of 2015. Webdev team worked incessantly to get the new site built. We were doing our own Q/A, load/stress testing, and getting the site ready for deployment to Azure. In some instances the webdev team was making UI &amp; UX decisions independently just so that we could get the product to a shippable place. It worked.

## Checking out and shopping carting

Webdev team did do the majority of the effort on developing what is the most important feature in the site: the ability to do commerce online. If it wasn't for the help of <a href="https://twitter.com/ClintCodes">Clint Carpenter</a> and <a href="http://slytrunk.com">Slytrunk</a> the cart and checkout flows would not have gotten built.  The talented programmers on Webdev team provided oversight on top of all of the core code contributions. Slytrunk's team was able to integrate with SBC webdev and Instrument without any hiccups due to processes that I brought to Specialized.

_[Pull requests were approved IRL](/images/approved.jpg)_

## Conclusive results.
In hindsight, it didn't really make much sense to spend all of that time doing custom software development for the ecommerce functionality. We spent months and months of time building features that have already been created.  We should have made the switch to an ecommerce platform, and then focused on UX and UI improvments.

On the upside we did see a substatial decrease in the bounce rate on our site, especially on mobile devices. We saw an increase in the amount of time spent on each page.  We also, after a big marketing push, saw an uptick in the number of ecommerce transactions that were completed.

Creating Specialized.com was one of the biggest challenges that i have faced in my career. I was, and still continue to be, appreciative of the opportunity to work on it, and with such wonderful people.  The lessons I learned, and experiences I had are ones that will continue to enrich my life for the years to come. I'm looking forward to the next one.
