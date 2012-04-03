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
