# JSCONF DAY 1: Thomas A. Valletta - The Web Console Game

On gaming.

* 63 million ps3s
* 65.3 million xboxes
* 95.35 million wiis
* 157.8 million smart phones in a single quarter

The nature of smart phones make the phone operate like a wii controller. Thomas made a bowling game that uses the phone as a controller using the gyroscope.

The game was made using HTML5 css3 transforms, websockets. For canvas he is using box2dweb which has a game loop. There is a tutorial:

http://github.com/tvalletta/web-bowling/wiki

Mobil web development can be tough, there are a few pieces missing. The good part about mobile is the fast iteration cycles. The bad parts of mobile development:

* Lack of WebGL
* Re-open page refresh
* App Cache offline doesn't work well
* Browser is bound to the OS (no auto updates)

# JSCONF DAY 2: Jake Archibald - Appcache: Douchebag

He built sprite cow.

Being online all the time creates problems when connections are not available. Apps assume persistent connection break when data is not available. When you make a site work offline how you manage it greatly impacts the end user experience.

Off-lining a "do stuff" site:

* add a manifest attr to the html tag
* the manifest is a list of files

## App Cache gotchas

The application cache takes over, connectivity doesn't factor into the app cache.

The application cache wont update unless the manifest file has changed. Any time you change a file you have to update the manifest.

Poor checking heuristics.

Don't change the url of the manifest; your html is going to get cached and people who see your html with the changed manifest url will never get the new updates.

The cache isn't updated until after new assets are retrieved which means that it will take two tries before the user sees the updated page.

The application cache doesn't like stuff thats not in the cache. Make sure to add things that shouldn't be cached to the network section.

App Cache has no clean up mechanism; no update or create without also caching the host page.

A hackey workaround is to create an offline.html page and load it on every page with an iframe.

# JSCONF DAY 2: Jarred Nicholls - JS on the GPU

He works at Sencha and is a webkit committer and a coauthor of the w3c web cryptography API (not yet released).

Running on the GPU is important for parallelization of computing. Why the GPU?

* It's fast, and geared towards parallel computing
* High memory bandwidth
* Specialized to mathematical operations

LateralJS is the library he made to experiment with this targeting OpenCL. They wanted full JS support for the project so they wrote a JS interpreter in OpneCL C.

OpenCL headaches:

* multiple memory spaces
* no recursion
* no standing libc libraries
* no dynamic memory
* no standard data structures
* buggy AMD/Nvidia compilers

Uses Esprima in V8 to get the AST.

# JSCONF DAY 2: Project Bikeshed

http://bike.sh/

bikeshed.js server side conversion of flash to JS.

Things you can do:

* You can make a simple turn based game
* The renderer can stream from the server
* Reuse existing flash content
* Edit existing flash content

They convert flash 9 & 10 and actionscript 3.

# JSCONF DAY 2: Christopher Chedeau - JSPP and the marriage of C++ and JS

You can write C++ and write it like it was JS.

He got JSON working in C++.

# JSCONF DAY 2: Brian Ford - Node.js

Is node.js better?

Organizations tend to perpetuate the problem they were created to solve.

* There are people who are afraid of change
* There are people who make change

node.js and JS in general are subversive, they are pushing change. When you put things in contrast when you compare them, controversy is entertaining, advocacy is criticism (when you say something is good you are saying somethign else is bad).

* Advocates are fanboys
* Critics are trolls?

We are not good at conflict, how do we improve dealing with conflict? Using science?

The correlation of the Q factor to the success of a broadway musical suggests that collaborating and challenge each other increases the likelihood of success.

Read "Thinking Fast and Slow". The slow deliberate part of our brain can be easily mislead, especially if you are uncomfortable. Programming is a behavioral science, a discipline where you use observation to solve problems. Programmers need to learn research methods so they can better arrive at valid solutions.

People are selfish, lazy, and easily bored.

Events vs threads is really apples and oranges. The fundamental technology underlying them is the same, its the implementation that causes the differences.

Computer literacy is the literacy of this century, claiming a technology is better because it has more people using it doesn't mean that it correlates to more people writing good solutions. We are trying to be effective at solving hard problems.

node.js rejects reality; multicore is the future, ignoring the ability to use multiple cores in a single process is ignoring this. An entire ecosystem of tools and libs must be created to approach new problems that JS was not intended for, not that JS can't - it's just missing the toolsets and libraries.

* Symmetric errors: are errors that you can track down
* Chain of errors: errors that can be tracked down

If we aren't careful about the chain of evidence we make it hard for people to understand and debug, we make it hard for them to solve problems.

It's important to understand and learn about concurrency, you don't have to pick a single approach just understand what is out there and the tradeoffs involved.

# JSCONF DAY 2: James Whelton - Changing the world one CoderDojo at a time

He is the head of CoderDojo which is like "the boyscouts of coding".

There was no introduction to computers until college and that had a 70% dropout. CoderDojo was born out of the frustration of the lack of coding in the education system. He wanted to make a "fight club" with keyboards.

Coder dojo:

* bring a parent if 12 or under
* loose session, self led learning
* relaxed atmosphere
* one rule: be cool
* kept money out of it
* got kids to bring their own laptops do kids could hack on their own machines at home
* get kids teaching other kids

To start it takes:

* Space
* Chairs and tables

The future of CoderDojo:

* improve infrastructure
* open data
* more tools
* more badges

# JSCONF DAY 2: Jacob Thornton - Brûlons les musées (burning down museums)

@fat author of bootstrap works at twitter and works on bootstrap, ender, hogan.js.


Eliminate the past. Read the futurists manifesto...

I got sucked into this talk and didn't take good notes, check out the video: #

# JSCONF DAY 2: Rick Falkvinge - Politics

The final talk.

- - -

cross reference with http://trevmex.com/
