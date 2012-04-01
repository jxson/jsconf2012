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


[hij1nx]: https://twitter.com/#!/Hij1nx
[dtrace]: http://dtrace.org/blogs/
[systemtap]: http://en.wikipedia.org/wiki/SystemTap
[darthBurrit0]: https://twitter.com/#!/DarthBurrit0