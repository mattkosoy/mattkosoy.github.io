---
layout:     post
title:      The hecka tight laptop set up method.
date:       2016-07-21 00:00:00
summary:    Tony Voorhees asked what my best practices are for getting a front end web development environment configured on a mac laptop. This summarizes my technique.
---

## TL;DR: 

* <a href="https://tonyvoorhees.github.io/">Tony</a> asked me for some help getting set up
* Fork and run <a href="https://github.com/thoughtbot/laptop">laptop</a>.
* Alias commonly used <a href="https://gist.github.com/mattkosoy/74b50b06787aa3a09d8c">git commands</a>.
* I like <a href="https://github.com/robbyrussell/oh-my-zsh">ohmyzsh</a> with the <a href="https://github.com/robbyrussell/oh-my-zsh/wiki/themes#pygmalion">pygmalion theme</a>. Sorry not sorry.
* Use <a href="http://ethanschoonover.com/solarized">solarized</a> as base color scheme.

## Introduction

A couple weeks ago my buddy <a href="https://tonyvoorhees.github.io/">Tony</a> asked if I could help him get his laptop set up for doing web development. There are a <a href="https://mallinson.ca/osx-web-development/">variety</a> <a href="https://www.smashingmagazine.com/2016/04/stop-installing-your-webdev-environment-locally-with-docker/">of</a> <a href="https://www.reddit.com/r/webdev/comments/45mkks/best_practice_web_development_environment_for_osx/"> approaches</a> for how you could go about doing this. This post is my suggestion for getting things set up relatively quickly and efficiently.  This post is not the _definitve_ way to get things set up. I'm not going to deep dive into some of the tangental topics that are spawned here. Those things are fodder for another post in the future. As always, you should always use the methods that works best for you.

<div class="clearfix">
<img src="/images/tony.jpg" alt="Mr. Tony Voorhees" />
<footer>Tony Voorhees</footer>
</div>

<a href="http://tonyvoorhees.com/">Tony Voorhees</a> is a San Francisco based artist, art director, and designer. He's been a friend and colleauge for just about twenty years now. He has over a decade of experience designing systems for small businesses, design agencies and product companies.  His most recent position was on the design team at <a href="https://www.draftkings.com/">Draftkings</a>.

<a href="/about">I</a> am the author of this website, and (more importantly) am <a href="https://www.instagram.com/explore/tags/zainabkosoy/">Zainab's</a> dad.

## Tony's workflow status quo. 

Tony mostly does interaction design, and because of that he hadn't spent much time adjusting his workflow.  It was easiest for him to use <a href="https://www.mamp.info/">MAMP</a> to do web development on his laptop. When his work was in a state of completion he would use an FTP app like <a href="https://panic.com/transmit/">Transmit</a> to transfer files to a server.  While this method can be leveraged successfully, there are other techniques that Tony could use to do this stuff.

Tony's a designer. He was put off by how the new-fangled tools are meant to work. I don't blame him. Using the terminal can be a bit overwhelming if you aren't used to it. The mamp GUI can be helpful to quickly configure and maintain a webserver. However it is much more efficient to use the terminal to do these things, and as I explained to Tony it's really easy once you understand the fundamentals.

## Terminal life and Laptop. 

The <a href="https://en.wikipedia.org/wiki/Terminal_(OS_X)">terminal</a> is a <a href="https://en.wikipedia.org/wiki/Command-line_interface">command line interface</a> application. You can do everything in the terminal that you can do in the finder, but faster and with even more control. Using the terminal is like driving a manual transmission automobile compared to an automatic. You have much more control over your experience. There are a ton of <a href="https://en.wikipedia.org/wiki/Comparison_of_terminal_emulators">different terminal applications</a> out there. I have used <a href="https://www.iterm2.com/">iterm</a> as my terminal for more than 5 years now. I still use the <a href="http://osxdaily.com/2011/01/03/split-terminal-mac-iterm2/">split pane</a> feature every day.

Now that I got Tony up to speed on what the terminal really was it was time to install some programs that are commonly used to do web development. I opened up a new tab in chrome and searched for "<a href="https://github.com/thoughtbot/laptop">Laptop</a> by <a href="https://thoughtbot.com/">Thoughtbot</a>. I greatly appreciate the open source things that Thoughtbot has put out there.

Laptop is an open source shell script that gets a mac laptop ready for doing web development. As the script was running in the terminal I opened the <a href="https://github.com/thoughtbot/laptop/blob/master/mac">source for laptop</a> in another browser window, and started to explain what each of the softwares this thing was installing on his machine. More on some of those things in a bit. 


You can install the Laptop script with this command:

    curl --remote-name https://raw.githubusercontent.com/thoughtbot/laptop/master/mac && sh mac 2>&1 | tee ~/laptop.log


## Customizations for your shell

After laptop has finished running I did some customizations to Tony's environment as the "last" part of the set up process. I am a huge advocate for taking the time to complete this part of the set up process. Doing this will give you more familiartiy with the command line tools, and along with that more confidence.

The first thing I do is install <a href="http://ethanschoonover.com/solarized">Solarized</a>. There is a <a href="https://github.com/altercation/solarized/blob/master/iterm2-colors-solarized/Solarized%20Dark.itermcolors">color scheme</a> that you can import into your instance of iTerm. There is also an instance for <a href="https://github.com/tomislav/osx-terminal.app-colors-solarized">the default terminal app</a> if you prefer to use that one. Either way I like using Solarized because the colors are easy on the eyes. I ususally install this color scheme for <a href="https://github.com/braver/Solarized">Sublime</a> too.

Since I am opinionated, and somewhat lazy I install <a href="https://github.com/robbyrussell/oh-my-zsh">Oh My Zsh</a>. The Laptop build script will change your shell to Zsh from Bash, and this framework makes it really easy to add some more customizations to your environment. The one thing I always do, and I did this for Tony as well, is switch the theme to <a href="https://github.com/robbyrussell/oh-my-zsh/wiki/themes#pygmalion">pygmalion</a>. The reason that I do this is because I, personally, like the git branch indicator status that is baked into this theme. I know that you can do this without using the Oh My Zsh framework but I am a little lazy. It's easier and faster for me to switch themes. Derp.

Alright. We're stoked. We're themed and colorized and solarized. What's next you ask? What's next is adding some customizations to your shell. We're going to add aliases for commands that we will be using very frequently during our workflow. The conifguration file for the shell is in a <a href="https://en.wikipedia.org/wiki/Hidden_file_and_hidden_directory#Unix_and_Unix-like_environments">hidden dot file</a>. We need to edit this file and add some stuff. Enter these commands into your terminal prompt:

    defaults write com.apple.finder AppleShowAllFiles YES
    killall Finder

This will reconfigure your system to display the hidden files that power your laptop. Pop open a new finder window, and press `shift + cmd + g` and enter into the prompt: `~/`. This will take you back to your home directory. It is the equivalent of typing in `cd ~/ && open .` into your terminal prompt. Try both methods just for fun! Now that your home directory is open, find the file called `.zshrc` and open it in a text editor.

Now comes the fun part. We want to add a couple of aliases to the environment that makes it really easy to enable and disable the visibility of the hidden files. Paste these lines in at or near the end of your `.zshrc` file:

    # Hide/Show hidden files in finder
    alias showfiles='defaults write com.apple.finder AppleShowAllFiles YES; killAll Finder'
    alias hidefiles='defaults write com.apple.finder AppleShowAllFiles NO; killAll Finder'
 
Save the changes, and then go back to your terminal and enter: `source ~/.zshrc`. This command reloads your shell instance and you will now be able to use the commands `showfiles` and `hidefiles` from your terminal. Boom, easy! 

Now what else can be done with this technique? One thing is to alias frequently used commands for Git. I worked with an awesome engineer a few years back and I have been using some aliases that he created. You can view them <a href="https://gist.github.com/mattkosoy/74b50b06787aa3a09d8c">here</a>. I usually save these into a new dot file in my home directory called `.gitaliases` and then load them in through my `.zshrc` config file by adding the following lines:

    # Import git aliases
    source ~/.gitalises

Dot file and system configuration is one of those things that everyone does slightly differently. There is a ton of <a href="https://dotfiles.github.io/">material</a> out there that you can read to gain more knowledge of how these things work. I am pretty sure that Tony is still using the methods that I illustrated here. So there are at least two other people out there who do things this way. 

## conclusion

At this point you're set up to do web development. <a href="https://github.com/thoughtbot/laptop">Laptop</a> has installed Ruby, Node, tools for interacting with Github and Heroku, tools for managing your system software, and even a couple of popular databases as well. And more.

The next things you could do are to talk about using a build system like <a href="http://gulpjs.com/">Gulp</a> to do automate your workflow.  Now that Laptop has been installed you could easily <a href="/2016/08/21/jekyll-is-great/">set up Jekyll and deploy your new site to github pages</a>.........Or not. 


