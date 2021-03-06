---
layout: post
title: "CoffeeScript: An Outsider Opinion"
date: 2011-07-03 18:16
comments: false
categories: Coffeescript, Javascript, programming
---

*Thoughts on CoffeeScript from a server-side developer just getting started with
frontend and JavaScript development.*

Firstly, if you’re unfamiliar with CoffeeScript, I recommend reading elsewhere
for a proper overview and introduction. The CoffeeScript homepage and the
Introductory Chapter of The Litte CoffeeScript Book are good resources for that.
If you’re really impatient CoffeeScript is in the author’s own words
"JavaScript’s less ostentatious kid brother." I’ve also heard it called
"Javascript for Ruby and Python programmers" and "What Javascript should have
been" by several of my peers. It also seems that it could’ve been called
CilantroScript[1] as it seems to have an instantly polarizing effect on people
in online communities such as Reddit and the Ruby on Rails community.

## So why did I start working with CoffeeScript? A number of reasons.

I am a backend developer and want to grow my frontend skills.
1. I’m starting to experiment with Node.js on the server.
2. Jeremy Ashkenas’s talk at CodeConf on literate programming blew my mind.
3.I know Ruby, so I should enjoy a “Javascript for Rubyists”, right?
4. It is going to be a Ruby on Rails default soon so I might as well check it
out now.
5. I like new and shiny things.

One of the quandries I faced when deciding to learn CoffeeScript was the fact
that I don’t know JavaScript. I spent 6 months noodling with Ruby before picking
up Rails and am still getting my feet wet with Python before taking Django for a
spin. So why on Earth would someone with my MO pick up CoffeeScript without
first becoming proficient with javascript? (Aside: I’m tired of the CamelCasing)
The answer comes from the first sentence (topic sentence, for those still in Jr.
High School) in the second paragraph of the coffeescript home page.

> The golden rule of CoffeeScript is: “It’s just JavaScript”.

As it turns out that isn’t entirely true since coffeescript is a class based
object oriented language and javascript is prototype based. This was actually a
mark against coffeescript for me since part of my desire to learn javascript was
to dally in prototype based OOP. (Luckily there’s still Io for that.) But for
the most part Coffee really is just javascript.

__EDIT: Jeremy Ashkenas has kindly clarified this point for me.__

> CoffeeScript is prototype based to the precise same extent that JavaScript is.
> The "class" keyword is just sugar for JavaScript’s constructor function +
> prototype chain combination. To mangle Shakespeare:
> 
> > What’s in a name? That which we call a class by any other name would smell
> > as sweet. Call it a prototype if you like — it’s the same thing in code.

Thanks Jeremy, apologies for misapprehending.

## So why the bother?

A while back I invested some of my hard-earned and short-in-supply cash to pick
up a ten-pack of PeepCode tokens. I have to say, I’ve derived an intense amount
of value from PeepCode but more on that later. I started with PeepCode’s Meet
CoffeeScript, had they produced a Meet JavaScript I would have started there,
but they didn’t. It took around six hours to watch the three and a half hour
video. Almost immediately after, I started PeepCode’s Meet Node.js screencast
and attempted to do it in javascript for about eight minutes. The appeal of
coffeescript was immediately clear.

In JavaScript, I have to worry about whether or not every line ends in a
semicolon, that there are no extraneous commas, yet commas where necessary,
and that I’ve remembered the var keyword on all my local variables. All that
stuff is important in JavaScript it doesn’t actually effect my application in
any way. In CoffeeScript, I can focus on the behavior of my code rather than the
presentation of it. Instead of scrutinizing each line for a semicolon and each
block for matching curly braces. I’m affirming that all my variables are scoped
properly and that my code does what I want it to do. It doesn’t add much to
javascript but rather, reduces the amount of worry and focus on what is at the
end of the day arbitrary stuff.

Sure, I have Vim configured with the fantastic Synastic plugin and I get
notified when I drop a semicolon or have an unmatched brace but what’s the
point? Basic sanity checking is all it can really do. Why even waste the time
to go back and insert those in the first place?

## Conclusion

I’m still continuing my education in JavaScript, CoffeeScript, jQuery, Node.js,
and prototype-based OOP. I’m armed with the beta copy of the CoffeeScript book
by Trevor Burnham from Pragmatic Programmers. I fully intend to use CoffeeScript
for all of my development in Javascript environments, server- and client-side,
work and play, for the foreseeable future.

## My CoffeeScript Resources
1. [The CoffeeScript Website and Documentation][1]
2. [Meet CoffeeScript][2]
3. [CoffeeScript: Accelerated JavaScript Development by Trevor Burnham][3]
4. [The Annotated CoffeeScript Source][4]
5. [The Little CoffeeScript Book][5]
6. [Javascript: The Good Parts by Douglas Crockford][6]
7. [Eloquent Javascript by Marjin Haverbeke][7]
8. [Smooth CoffeeScript by autotelicum][8] via
[@Raynos2](http://twitter.com/raynos2)

[1]: http://coffeescript.com
[2]: http://peepcode.com/products/coffeescript
[3]: http://pragprog.com/book/tbcoffee/coffeescript
[4]: http://jashkenas.github.com/coffee-script/documentation/docs/command.html
[5]: http://arcturo.com/library/coffeescript/index.html
[6]: http://oreilly.com/catalog/9780596517748/
[7]: http://eloquentjavascript.net/
[8]: http://autotelicum.github.com/Smooth-CoffeeScript/
---

1. Cilantro (or Coriander) is an herb which to some people tastes pleasantly
citrus-like and to others is rank and revolting or soapy. As a result many
people either love it or hate it. Few are ambivalent about Cilantro. The same
is true of CoffeeScript in my observation.
