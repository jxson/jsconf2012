# NOTCONF: 2:00-2:30  PAOLO FRAGOMENI

> Deep inspection of the operating system and its processes in realtime using JavaScript. As well as several other unexpected uses of our favorite yet unusual language.

Use [DTrace][dtrace] for holistic instrumentation, there are node bindings for [DTrace][dtrace].

* https://github.com/bcantrill/node-libDTrace

And there is a [DTrace][dtrace] lib that will allow app specific instrumentation:

* https://github.com/chrisa/node-DTrace-provider

Monitoring is insufficient

* It assumes arbitrary data points are interesting
* Doesn't take responsibility at critical time

I take this to mean that monitoring at arbitrary points won't help you figure out what caused a catastrophic failure. Paolo suggests using a core dump to help in the postmortem.

An interesting point made during the QA was that you can use json streams in [DTrace][dtrace] scripts!

[@hij1nx][hij1nx] mentioned trying to use [SystemTap][systemtap] where [DTrace][dtrace] is unavailable, [DTrace][dtrace] is available on osx and smartOS.

# NOTCONF: BRIAN LEROUX on using Weinre

Awesome for debugging mobile web apps

* http://phonegap.github.com/weinre/

I have used this in the past on a little game prototype I have been working on with [@DarthBurrit0][darthBurrit0] and it worked really well for debugging touch events. I am excited that work on this is moving forward and that this will work on things like blackberry, etc.

# NOTCONF: 3:00-3:30 PAMELA FOX

> Why ternary operators make me want to kick someone in the nuts: AKA code readability.

In the world of JS lins there are

* Authors
* Users

Most of us use a ton of libraries

Nested ternary operators make it hard to use libraries, they make them hard to read and hard to debug. As a user they also make one feel like they are outside of the in-crowd, libraries should be more inclusive and make users feel like they are part of the party.

Stages of being a user:

* learn how to use the library (docs)
* debugging when things go wrong
* workflow integration

Documentation should be accurate and easy to patch but not fragmented (multiple sources documenting the same thing, there should only be one true source).

To help with debug-ability make your code easy to read, use descriptive variable names, and debuggable on all platforms. Don't use shortened variable names, code for other people! Use semicolons to help aid in the readability, people working on and reading your lib shouldn't be experts in the way the JS parser works.

Does your lib holdup to other people's linters? Will it break if concatenated and/or compressed? Is it easy to get contributions? How do you handle coding, building, are tests easy to run?

Do you want elite code practices that exclude potential authors or users, or do you want a library that is more inclusive and has more potential for adoption and contributions?

# NOTCONF: 4:00-4:30  CHRIS WILLIAMS

> How to attend a conference. No seriously, stop spending money attending shitty conferences and attend awesome ones.

Go home and set up your own conference. How to not put on a typical event. Stop going to confs that cost a lot of money. When confs become businesses our only vote is our dollars, confs should be community events not profitable ventures.

Community events are vitally important to the ecosystem. Domain speciality is not required to put on an event.

Talking about conferences that cost a ton of money: instead spend the money to fly to the place, stay with friends, save your money. Find people who went and make some friends. Turn confs into community events! Go out and find the speakers, go to the parties, find the speakers and ask them to go to the "other bar". The "other bar" is a chill place where you can talk, establish relationships, etc.

Don't let "regurgitation events" take over, don't pay for things that you can just watch on the internet. We need events that bring to bear new talent and technology that try to make us better. Speaking needs to be done on new topics, not the same things over and over. This should be about starting a dialog.

[hij1nx]: https://twitter.com/#!/Hij1nx
[dtrace]: http://dtrace.org/blogs/
[systemtap]: http://en.wikipedia.org/wiki/SystemTap
[darthBurrit0]: https://twitter.com/#!/DarthBurrit0
[pamelafox]: https://twitter.com/#!/pamelafox
[chris]: https://twitter.com/#!/voodootikigod