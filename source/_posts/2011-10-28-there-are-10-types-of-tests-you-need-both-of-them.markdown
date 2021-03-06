---
layout: post
title: "There Are 10 Types of Tests. You Need Both of Them"
date: 2011-10-28 02:22
comments: true
categories: Ruby TDD programming
---
Over the course of the last year, and especially in the last two to three months
I have been internalizing and witnessing for myself the extreme benefits of
accompanying your code with a test suite which matches your code in quality.
By this I mean that it is difficult (and damn frustrating) to write good tests
for poor code. At my current skill level as a programmer there's code in my
primary code base that is so bad (yep, I wrote that code too) that I am unable
to write good tests for it. Up until four or five weeks ago, coinciding with my
second readings of [The RSpec Book][1], and [The Cucumber Book][2], sitting in
as a guest panelist on [Ruby Rogues][3], and watching a bunch of
[Destroy All Software][4], I realized that in order to gain the benefits of TDD
being touted by some of the most respected members of the Ruby community, I
needed better tests. Specifically better isolated tests.

## Isolated Tests
I recently had to completely justify my desire to add and grow isolated tests
for production code. The argument against doing so was simply that if the *whole
point* of isolated tests is to know when something breaks in the future, an
integrated test suite will pick up those failures just as well. Therefore
isolated tests are a waste of time and engineering effort.

This argument *is* correct, provided the only thing you use your isolated tests
for is protection from regressions. However, doing so leaves out what is to my
mind the __greatest__ and most profound advantage of isolated testing, which is
immediate, focused feedback. I definitely think I'm inventing terms here so
please indulge me while I clarify them.

- Immediate: *The result (success or failure) can be observed right away.*
- Focused: *The cause of any failure is known to be within the system under
test.*

Anyone who has worked in software for a substantial amount of time knows that
we are each our own worst enemy and the temptation to add unnecessary complexity
is a constant bother. How many of us have added arguments to methods only to
use the default value every time. I call these bullshit arguments, because they
piss me off when I have to put up with them. The joy in a test with truly
immediate feedback is the laser focus that they give you when working on a
system. You're literally doing one thing at a time and checking that you get the
expected result even when it isn't success. When you get the failure you expect,
you simply move on, and when you get an unexpected failure it causes you to
identify the disparity between your mental model of the system and the computer
model and correct it. Since these tests are isolated and generally run in less
than a second, there is essentially no penalty for running the tests with
monstrous frequency. When you do have to stop, it is to make a correction,
even if it is just a mental correction. The time you save fixing it early is
more than enough to justify the low cost of running the test.

One of the downsides of this type of testing is that you are treating anything
which isn't the system under test as an external service and therefore
stubbing the interactions with it. This works great for fast, clean-room tests
but it means that the burden of ensuring that the assumptions you make in one
test are validated in the respective tests for your other systems is entirely on
the programmer and since programmers are human, this will eventually lead to
mistakes.

My personal favorite aspect of isolated tests is how informative they can be
about your system. It's pretty common knowledge that if your tests are a pain in
the ass to write, it's a good indication that your code is too-tightly coupled
and refactoring to follow the [Law of Demeter][6] and [SOLID][7] design
principles is a good idea.


## Integrated Tests
One of the scariest things that happened to me in recent memory was discovering
that people were surprised when after arguing in favor of getting higher quality
unit tests I was still unsatisfied because our integrated tests also needed
attention and improvement. I found this a little disturbing (okay, I found this
really disturbing) because I can't imagine how long it would take to manually
verify that I didn't overlook anything in the major refactoring or feature
addition I just performed. I certainly don't budget the time to manually test
every resource and parameter combination by hand. I might do so initially
because a major disadvantage to integrated tests is in the difficulty of doing
exploratory testing at this level. As a result, when writing integrated tests, I
tend to rely on manual experimentation to determine how my system behaves in
undefined situations, make a decision on the appropriateness of that behavior
and then solidify that set of interactions into a group of tests. One of the
nice things about integrated tests is that once written, they tend not to change
unless your expected end-user behavior changes. This is afforded by the
"bigger picture" nature of integrated tests where you are less concerned with
the exact behavior of any one unit and instead are validating the result of
system-wide operation and interaction. Thus, integrated tests are largely immune
to internal refactoring.

As one can imagine, the strengths of isolated tests are the weaknesses of
integrated tests. When something is wrong, particularly in a complex interaction
that touches many parts of the system, it can be unclear exactly where the
problem in the codebase is when an integrated test fails. If you get an actual
exception, you'll have a stacktrace to guide you, but those tend to be unhelpful
errors like an unexpected nil and rarely is it obvious at what level the nil was
assigned and how long it had been propagated upward until the failure. So it
can be said that integrated tests are not focused since there is no indication
of precisely where in the system the failure has occurred. Additionally,
integrated tests mandate that you test your full software stack. Any persistence
layers, external services, background tasks, and other specific tools you're
using should be tested during this phase. As you can imagine testing all of
these things takes time and computing power. It is not feasible to expect even
a subset of an integrated test suite to run in the same magnitude of time as
isolated tests, what this means is the tests are no longer immediate. Thus,
they are not suitable for running at every pass of your TDD cycle. Only when you
believe the feature to be complete.

## Conclusions
So if isolated tests don't identify incongruities between subsystems and
integrated tests are too slow to run during an immediate feedback TDD cycle,
which do you use? As you may have surmised from the title, the answer is...
both.

[The Cucumber Book][2] suggests that "It's sometimes said that unit tests ensure
you 'build the thing right', while acceptance tests ensure you 'build the
right thing'." I also like Avdi Grim's simile of mocks being like hydrogen
peroxide in that they both fizz up around problems.

With our twin goals of systematic coverage and focus during development in mind,
let's recap how each set of tests is used.

When you know what you you're building but not how, reach for the integrated
tests. Define the desired outcome at the high level and then run that test again
when you think you've got it down. Start thinking about the different aspects of
that problem and decomposing them. Then devise a system of smaller tests
mirroring the smaller objects and functions you'll use to accomplish that goal.
Isolated tests are there once you're ready to do exactly that. There to aid
you in that mission and guide you toward good design decisions. "I'll do what
the tests tell me" is not an uncommon phrase from me.

*Isolated regression tests are a side effect of good TDD, they're more important
during the process than after.*


*Integrated tests are the ones you bring home and show your mother. The ones you
can be proud of at the end of the day.*

[1]: http://pragprog.com/book/achbd/the-rspec-book
[2]: http://pragprog.com/book/hwcuc/the-cucumber-book
[3]: http://rubyrogues.com/book-club-exceptional-ruby/
[4]: https://www.destroyallsoftware.com/screencasts
[5]: http://nowbox.com
[6]: http://avdi.org/devblog/2011/07/05/demeter-its-not-just-a-good-idea-its-the-law/
[7]: http://blog.rubybestpractices.com/posts/gregory/055-issue-23-solid-design.html

