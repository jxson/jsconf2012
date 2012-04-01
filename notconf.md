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

[hij1nx]: https://twitter.com/#!/Hij1nx
[dtrace]: http://dtrace.org/blogs/
[systemtap]: http://en.wikipedia.org/wiki/SystemTap
[darthBurrit0]: https://twitter.com/#!/DarthBurrit0
[pamelafox]: https://twitter.com/#!/pamelafox