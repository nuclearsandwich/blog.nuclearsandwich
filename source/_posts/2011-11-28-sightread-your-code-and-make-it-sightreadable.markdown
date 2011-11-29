---
layout: post
title: "Sightread Your Code and Make It Sightreadable"
date: 2011-11-28 15:28
comments: false
categories: programming music
---

*Sightreading is an essential skill for any musician. Turns out it's pretty
important for good software developers as well.*

## What is sightreading? ##

I've been listening to a ton of [Ruby Rogues][1], so let's begin with a
definition.

From Wikipedia,

>  __Sightreading__ *is the reading and performing of a piece of written music,
> specifically when the performer has not seen it before.*

Musicians are always evaluated on their ability to read and interpret musical
scores on command, a musician's time isn't cheap and rehearsing a specific piece
of music is a privilege reserved often reserved for school ensembles and AAA
film score recordings. I exaggerate a little, but honestly, professional
musicians are not afforded a lot of rehearsal time. They are instead expected to
walk up to a piece, play their bit expressively while fitting in with the rest
of the ensemble perfectly, sometimes without ever hearing them.

If you're wondering how on Earth this could possibly relate to software, look no
further than your first day on your current project. Most software developers
don't have the privilege of starting from scratch when they begin a new job or
contract.  Instead we are thrown into an existing one and expected to decrease
the bug count. Some people might say that's an unfair expectation, but it is, in
fact, no different from expecting a professional musician to walk into the
studio, read your score, play their piece once or twice, then collect their
check and leave.

Western music has a complex but accepted system of notation that all musicians
and composers are expected to be familiar with. On top of this base language
there are sets of idioms particular to certain genres. By writing works in this
language and leveraging (often subconsciously) these idioms composers create
music that musicians can read and follow and interpret even *as* they play.

In the case of software development, the language and idioms are still present,
but they are the languages and idioms of computer programs rather than those of
western music.

## Sightreading Code ##

So what's the point of sightreading code? Here's three scenarios from every
stage of one's career.

1. You're fresh out of University and in a technical interview. You've been
	 asked to find and fix the two known bugs in a text formatting program.
2. You've just started your first day at a new job and you've been tasked with
	 extending an existing project with new features.
3. You're a super celebrity master contractor and people pay you way too much
	 money. You walk up to code you've never seen before and need to make magic
	 happen in order to justify your absurd cost.

In each case your value hinges on picking up a brand new codebase and running
with it. Since you can't control the quality of code you didn't write you can't
make any excuses regarding what's already written. At this point you have two
options. Skim the code, or read it all.

I will tell you right now, __skimming doesn't work.__ You can't read every other
line or seek for specific variable names and actually follow what is going on.
When you do so, you screw it up.

*Disclaimer: Slight boorishness follows*
> If you ask me a question about my code, I'm going to assume you've read every
> relevant line.

Relevant lines are tough to pin down, but at the very least the entire method in
question is a good start. When you haven't done so, it's plain disrespectful and
arrogant on your part, especially when your question is answered (or nullified)
by something directly in that body of code. By skimming and then bringing up
something you saw during the skim, you waste your time and mine.

Everyone who has taught me up until a year ago will roll their eyes at me for
this because I was the best at skimming (meaning I was the worst reader/pupil) I
actively avoid jumping to conclusions about what I read and take a concerted
effort to answer as much as I can on my own before escalating a problem.
Furthermore, when I do I often have a much better handle on what question I am
asking than I would otherwise have had.

In all seriousness, when you do this I start to think about spending less time
with you. I warn everyone I'm comfortable warning not to skim ___ever___.
Including you, dear reader.

Since skimming code doesn't work, our only remaining option is to actually read
the code completely. This probably sounds like a lot of work, that's because it
is, but so is reading and performing an entire ten minute piece in half an hour
and musicians still manage to get it done.

## Making your Code Sightreadable ##

- so others can sightread it
- so you can sightread it
- Composed method
- Tell don't ask
- Law of demeter

[1]: http://rubyrogues.com
