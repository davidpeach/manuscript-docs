# Introduction

## What is Manuscript?

Manuscript is a little tool that attempts to make the process of building and testing php composer packages as simple and as automated as possible.

At its heart, it just wants to help you scaffold composer packages and make it a breeze to install that package-in-development into a local framework. It does this via the composer path repository symlink functionality.

There is nothing crazy going on under the hood. And I’m always looking for ways to improve it and make it as helpful as it can be.

But I don’t want it to develop feature creep.

Early on in it’s development I had visions of it being this big thing that could help with commit changes / switching between package versions etc. But I have come to the decision that I just want it to remain a simple tool.

## Why build it?

I was building a laravel package for work and set up a  local laravel installation and used the path repository setting manually. It’s pretty easy to set up, once you know how.

Then I had an idea for another package I wanted to build. So I went through the same process of setup.

At that point I thought “I wish there was a way to make this process quick, easy and as automated as possible”...

...lightbulb moment.

I did have a quick search for tools and didn’t find anything at the time. So I began trying to make my own.

It’s been through various iterations -- and has changed a lot -- but all within the same repository.

Through the course of building myself a little tool, it has become more of a passion project that I hope can help the wider php community.

