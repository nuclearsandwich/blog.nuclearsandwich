---
layout: post
title: "Sightread Your Code"
date: 2011-11-29 09:50
comments: false
categories: programming music
---

*Sightreading is an essential skill for any musician. Turns out it's pretty
important for good software developers as well.*

## What is Sightreading? ##

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

In order to determine how we can become more effective code sightreaders, we
again look to our musician friends who have been doing this for some time.
Musicians who want to improve their sightreading do the following things.

### Musicians Know and Practice Scales ###

Musicians who practice their scales are the ones with the best technical chops,
their fingers are the most agile, their articulation superb and they're
comfortable with any given set of notes.

For programmers who wish to improve sightreading, there's simple no replacement
for knowing the language you're in. If you've never looked at C before, you'll
spend 20 minutes figuring out what `int main() {` is, or spend that time
figuring out the precise semantics of a line ending conditional in Ruby.

*If you don't know the language, you'll spend time figuring out what the
language is doing instead of what the program is doing. Know your language.*

### Musicians Study Music Theory ###

Every musician who works with written music needs at least a basic understanding
of music theory. Without it, reading music, let alone interpretting it, is
impossible. Over time many musicians gain an intuitive understanding of theory.
They realize all major scales are the same but starting from a different note,
then slowly absorb more as they go. But some of the best musicians actively
learn theory as theory and can leverage that to do amazing things as Jazz
improvisers, composers, and virtuosos.

As computer scientists, we need to know the design patterns used in our field.
Decorators, strategies, delegation, they all need to be second nature if we
intend to approach a new body of code and immediately see what's going on.
Additionally, these patterns establish a common vocabulary you can use to
discuss code with other programmers regardless of their language and experience.
If you both know the patterns, they can add precision and expressiveness to your
non-executable communication.

*Knowing patterns allows you to see and apply them instantly when you enter a
new codebase or team. Use them as a common vocabulary.*

### Musicians Sightread During Practice ###

Lastly, and hopefully most obviously, musicians practice the act of sightreading
during their own self-directed practice. My high school band director, once said
to our ensemble that if you do something for the first time during the show,
you're practicing in front of a live audience, not performing.

Likewise, don't assume that if you know your languange and some patterns you'll
be an extraordinary sightreader. You need to apply that knowledge frequently if
you want to temper it into skill. Trust me, you do *not* want to do it on the
job your first few times. If you do, you'll likely feel rushed and sink back
into skimming. So find an open source library you use, pop into it's source code
and get reading.

*Don't do your practicing in front of a live audience. Read open source code in
order to get better at sightreading.*

## Wrapping Up ##

Thus far I've made the assumption that you will have no control over the
codebases that you sightread. While this is often the case when starting out,
we often spend a significant amount of time with one codebase and start to grow
into and learn it. While this certainly helps, one of the main differences
between musical scores and software projects is that individual scores seldom
change between performances whereas software is in constant flux. If you wrote
it a week ago you'll be sightreading it again next week. If you wrote it a month
ago, how many hands have been at it since you last looked at it? Sightreading is
a constant and ongoing process in software.

As a writer of software, you can and should take steps to make your software
more sightreadable but I've throw a big wall of text at everyone so I think
I'll tackle that subject at a later date.

[1]: http://rubyrogues.com
