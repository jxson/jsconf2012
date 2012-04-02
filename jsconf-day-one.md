
# JSCONF DAY 1:

There is no concurrency in the browser but as a side effect of the design of JS that makes JS devs are good at concurrent programming.

WebWorkers are a bit heavy for concurrent and are only good for apps that do not need to use shared state. There is a high communication cost between concurrent operations with WebWorkers.

Ideally the programmer should be able to tell the jit that something can be done in parallel. River Trail tries to do this, looks like JS, behaves like JS, and has a rule of "no surprises" and maintains JS security model.

It has a deterministic execution model:

* no race conditions
* no data lock
* no magic

They are really interested on getting feedback from developers on this new extension to JS. Are there problems with it? Will devs like it?

River Trail is available as a Firefox extension for anyone who would like to play with it.

[river]: #
