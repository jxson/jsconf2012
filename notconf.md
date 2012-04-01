# NOTCONF 2:00-2:30  PAOLO FRAGOMENI

> Deep inspection of the operating system and its processes in realtime using JavaScript. As well as several other unexpected uses of our favorite yet unusual language.

spire should define upfront what it means by realtime, when realtime is appropriate. When there is latency the experience should degrade and not cause a catastrophic failure.

use DTrace for holistic instrumentation, there are node bindings for DTrace.

* https://github.com/bcantrill/node-libDTrace

DTrace lib that will allow app specific instrumentation:

* https://github.com/chrisa/node-DTrace-provider

monitoring is insufficient

* it assumes arbitrary data points are interesting
* doesn't take responsibility at critical time

I take this to mean that monitoring at arbitrary points wont help you figure out what caused a catastrophic failure. use a core dump to help in the postmortem.

You can use json streams in DTrace scripts.

@h1j1nx use SystemTap where DTrace is unavailable, DTrace is available on osx and smartOS.
