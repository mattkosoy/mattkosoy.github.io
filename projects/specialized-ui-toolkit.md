---
layout: page
title: Specialized UI-Toolkit
permalink: /projects/sbc-ui-toolkit
summary: An experiment with atomic design
tags: project
page-category: project
image: /images/ui-toolkit.png

---

# A kit of parts for all of the digital things

<div class="clearfix py3">
  <img src="/images/ui-toolkit.png" alt="SBC UI-Toolkit" />
  <footer>The ui-toolkit homepage.</footer>
</div>

## Innovate or Die

One of the new things I introduced to Specialized was the concept of <a href="http://bradfrost.com/blog/post/atomic-web-design/">atomic design</a>. For those that don't know this is a design practice that breaks down a web page into a <a href="http://bradfrost.com/blog/mobile/bdconf-stephen-hay-presents-responsive-design-workflow/">series of components</a>.  Following this approach was crucial to the successful, and timely relaunch of <a href="http://www.specialized.com">Specialized.com</a>.

The effort started in April when I began, on my own time, to experiment with <a href="fbrctr.github.io">Fabricator</a>, an open source tool for rapidly developing user interface elements created by <a href="lukeaskew.com">Luke Askew</a> Armed with Luke's open source software I was able to articulate my vision to Specialized's Director of Technology, and to several senior memebers of the Marketing team. This group of leaders agreed that leveraging atomic design principles was the correct choice for the business. My effort enabled Specialized to communicate to our partner in design, <a href="http://instrument.com">Instrument</a>, what the brand needed to be successful with the redesign effort. 

## A Prototype presentation

In June of 2015 I, along with several of my teammates, was sent to Portland to meet with Instrument's team. During  the brainstorming sessions I was able to do a demo of my very rough ui-toolkit prototype. These sessions sparked a conversation that eventually turned into the lexicon for us as we spoke about the "pages" in the site.  Instrument's strategy team defined, approximately, 5 "pages" or so that we would begin to use.


1. The homepage
2. Gridwalls
3. Stories
4. Product Detail Pages
5. The shopping cart

<div class="clearfix py3">
  <img src="/images/ui-toolkit-page.png" alt="a PDP sample" />
  <footer><cite title="pdp">A sample of a Product Detail Page</cite></footer>
</div>


Of course there were more pages than just this, but these 5 were the core. Instrument, along with these static page examples, also provided us with a variety of components that Specialized's Webdev team could use build pages with as well. The toolkit is very well organized using a "components", "structures, and "pages" taxonomy. In the context of atomic design a component is an "atom", a structure is a "molecule".

<div class="clearfix py3">
  <img src="/images/ui-toolkit-gridwall.png" alt="gridwall structure" />
  <footer>A tile grid "structure"</footer>
</div>

## It's alive!

We had created a living, breathing, static website thing. It made it easier to communicate the UX details in a way that a traditional wireframe couldn't. We were able to demonstrate the more subtle points of the site: animations, button states, carousel transitions in the web browser. This process also made it much easier for us to do  our testing on mobile devices.

Another benefit for having built our front end in this way was that we kept our concerns separated. We had ~~all~~ most of of our clientside things contained in the toolkit. We had the look and feel contained in the toolkit. We were able to demo changes, bug fixes, and new features with no risk of breaking the production app. Speaking of the production app, we did our integrations through a private <a href="https://www.npmjs.com/">NPM</a> module that I set up.

Midway through our sprint to deliver <a href="http://www.specialized.com">Specialized.com</a> we had to create a new <a href="/projects/specialized-cms">content management system</a> to handle the needs of the new content strategy. This project was a great way to put the ui-toolkit into practice. The kit of parts kept the look and feel of these two software products consistent. Having the CMS work responsivley was hugely appreciated by the content management team.

## Conclusions

This experiment with atomic design proved to be successful, in my mind. The kit of parts is in use now as a digital standard for Specialized. Keeping the front end code seperated into it's own application proved to be a benefit. The ui-toolkit continues to evolve as new features are added to <a href="http://www.specialized.com">specialized.com</a>.
