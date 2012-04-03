
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

# JSCONF DAY 1: Panel - Diversity in Communities

Diversity isn't really talked about.

Young people are impressionable and believe in the "status quo". Holisitc approaches need to be applied that avoid singling out specific incidents.

Diversity helps create a larger pool of talent, lacking diversity means less people hacking. Having different kinds of people brings different backgrounds and experiences.

Only 14% of women are CS grads, only 2% in open source. The problem revolves around pooling. If more people start in the beginning then there will be more people available to the pool later.

Change takes time, it's important to make an impact with the people you know so that they are aware of the possibilities so they don't self select out.

# JSCONF DAY 1: # - A day of life in V8

He encourages devs to look under the hood of V8 and get involved.

It is possible to see what V8 does by using the decompiler. It is good to write your app and then analyze it to see how JIT handles it, its possible to optimize your code but it's good to pass bits of slow code along to the JIT writers; V8, FF, etc.

# JSCONF DAY 1: # - Mojito

Yahoo devs thinks the web is broken, cause they are some of the guys who break it. When you connect on slow networks stuff doesn't work. Always assume your website will have to run without JS to be accessible. Mobile is a big deal, 6 billion users.

Progressive enhancement: start with the basic and add on top of it. Think about electric toothbrushes, if they run out of power they still work as a toothbrush.

# JSCONF DAY 1: Remy Sharp - Build Anything

We now have a web stack that really allows you to build almost anything. If it doesn't exist we know how to make it. There is bleeding edge technology available today.

Integration with the desktop needs to be more fluid. You can make your apps more "apish" using progressive enhancement:

* `<!DOCTYPE html>`
* Web storage
  * the solution to cookies, not a solution to app cache
  * they have events that get sent to other tabs - SYNCHRONIZATION
* validations
* History API
* AppCache
  * for caching specific objects it is better since it will allow your items to not be pushed out by the browser caching apps on other domains.
* WebSockets
* Drag and Drop

look up webrt

# JSCONF DAY 1: David Nolan - Closure Script / Jelly Stains

It's worthwhile to learn some kind of lisp. Programming languages are tools.

People can only really manage 7 plus or minus 2 things at once. We learn to architect by building during play, like playing with legos. There should be no difference between your ideas and the code you develop.

Read the reasoned schemer

We need to play with other languages to learn how to make JS better. Community is about shared ideals not holding onto specific tool sets.

# JSCONF DAY 1: Daniel Henry Holmes Ingalls, Jr. - Modern Object Oriented Programming

This guy wrote smalltalk! His talk is on the live web, what it would be like to write squeak small talk in the browser.

Look up The Lively Kernal.

* A component architecture
* Runs in any browser
* Composition environment
* 

[river]: #