---
layout: page
title: Conjuring up a new content management system for Specialized Bicycle Components.
permalink: /projects/specialized-cms
summary: Can you create a robust CMS system with no time or budget? No problem.
image: https://www.dropbox.com/s/uwcg17i5bktg88n/Screenshot%202016-06-07%2010.28.34.png?dl=1
page-category: project
---

# Work with what you got

Along with the delivery of <a href="/projects/specialized-dot-com">dot-com</a> my team also had to create a custom CMS system. Specialized has an entire team of content managers who work tirelessly to translate our rich contentinto their own localized flavor. Webdev needed to provide a solution to this marketing team which would enable changes to be made to the website swiftly and easily.
  
There was a choice to make at this point: build these features into the legacy systems, or create a new CMS from scratch using nodejs. We chose to use nodejs.
 <!-- -->

<div class="clearfix py3">
<img src="https://www.dropbox.com/s/oyctlvyvlqrht9a/Screenshot%202016-04-05%2011.21.24.png?dl=1" alt="the story translation tool" />
<footer>Screenshot of a translation tool in the CMS</footer>
</div>

## The challenge at hand

The was a team of eight or ten people, including myself, who worked on this project. The big challenge was the very narrow window we had to execute. Time waits for no one, and thus I began the build by creating a fork of the node app that we were using to build the other project: our new corporate web site. I quickly started peeling back the things. In about an hour and a half I had a "boilerplate" node app in a private github repository that I shared with my colleauges.

We designed this content managements system to use a separate restful api to conduct its buisness operations such as storing and retriveing content from the database. One the many things that I did was help to provide clarity, constantly, into what this API and its endpoints should look like. It was really nice to be able to utilize the `.yml` files that we had in our <a href="/projects/ui-toolkit">ui-toolkit</a>. The fields in these files acted as a blueprint, of sorts for our interface and for our API.

The interface itself was rather easy to build. I used all of the patterns that were defined in our <a href="/projects/ui-toolkit">ui-toolkit</a> on the CMS UI. The look and feel of the forms was identical to that of the public facing site. Same typeface, same everything. I made the  UI responsive by leveraging a 12 column grid built with flexbox.

## Testing to the rescue 

<div class="clearfix py3">
<img src="https://www.dropbox.com/s/uwcg17i5bktg88n/Screenshot%202016-06-07%2010.28.34.png?dl=1" alt="testing bugs in the CMS" />
</div>

One of the most painful challenges of the CMS build was the short period of time that we had with which to execute.  The compression created a "wild west" type of atmosphere where features would be built by any/all means necessary.  Some of the frontend was build with ES6, and some with ES5. Different parts of the CMS had different "personalities" based upon who the author of that part was. It became messy rather quickly. After we launched the <a href="/projects/specialized-dot-com">corporate site</a> we were able to refactor the cms to use ES6 syntax

The guiding lights in our case was two things: 1) implementing a test driven development process, and 2) using `eslint` to keep the code consistent, and standardized. Bonus points for the number two was getting to learn new things on the job.

## Results of the effort

To summarize the result of the CMS sprint, which lasted about 6 weeks, was a successful release of a new service driven CMS for Specialized. The new CMS has a responsive UI, and maintains a similar look/feel as the <a href="http://www.specialized.com">Specialized</a> site itself. A team of 8 collaborated and exectued on a tight deadline. Our effor changed the way Specialized did it's content management on the internet.

<div class="clearfix py3">
<img src="https://www.dropbox.com/s/wvdw7fo233ezqbm/Screenshot%202016-03-17%2011.38.58.png?dl=1" alt="Lots of +1's" />
</div>
