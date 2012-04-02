
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

# JSCONF DAY 1: Andy Wingo - Stranger in These Parts

Andy is a compiler nerd who works for Igalia, he has been working on JavaScript core and V8.

Languages are tribal, they have elders, in group - out group.

Look up DFG and LLInt.

JIT compilation is a speculative optimization. LLInt is the new low level interpreter for JS core that was rewritten and has parts in Ruby.

Lazy bytecompilation parses the bytecode on the first call.

## Why was JS core rewritten?

* Control of stack layout
* Control of code

It happens to be much faster. This helps out in situations where native code isn't allowed to be compiled from your application (ios), having a faster JS interpreter helps in these situations.

http://wingolog.com

# JSCONF DAY 1: Paul Irish - JavaScript Tooling

Tools around rich web app development.

We are speinding too much time around common tasks, we should avoid spinning our wheels and instead work on the experience we create.

Tools like css and template compilers help a bit. Languages that compile to JS can also help.

On iteration and workflow new tools in chrome's dev tools help. Source maps will help debug things like minified JS, CoffeeScript, less, stylus: anything that has a source map.

Look up grunt


[river]: #