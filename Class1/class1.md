# React-in-depth

### what is emmet?

> Emmet is a free add-on for your text editor that allows you to type shortcuts that are then expanded into full pieces of code.

### Difference between library and framework?

> Library: Easy to add in our code

> Framework: Need some effort to implement

### What is CDN, why do we use it?

> A Content Delivery Network (CDN) is a critical component of nearly any modern web application. It used to be that CDN merely improved the delivery of content by replicating commonly requested files (static content) across a globally distributed set of caching servers

> CDNs do a lot more than just caching, now they deliver dynamic content that is unique to the requestor and not cacheable. The advantage of having a CDN deliver dynamic content is application performance and scaling. The CDN will establish and maintain secure connections closer to the requestor and, if the CDN is on the same network as the origin, as is the case for cloud-based CDNs, routing back to the origin to retrieve dynamic content is accelerated.

> Any kind of file can be served as static content as long as it does not change in response to a user’s actions or inputs. This includes images, JavaScript files, CSS files, videos, Flash files, even web pages.

### Why is React known as React?

> Declarative ->
> We don't need to manipulate the dom by ourselves

> Component Based ->
> Build encapsulated components that manage their own state, then compose them to make complex UIs. You can easily pass rich data through your app and keep state out of the DOM.

> Learn once write anywhere ->
> You can develop new features in React without rewriting existing code.

### What is crossorigin in script tag?

> The CORS behavior, commonly termed as CORS error, is a mechanism to restrict users from accessing shared resources. This is not an error but a security measure to secure users or the website which you are accessing from a potential security breach.

> Cross-Origin Resource Sharing (CORS) is an HTTP-header based mechanism that allows a server to indicate any origins (domain, scheme, or port) other than its own from which a browser should permit loading resources. CORS also relies on a mechanism by which browsers make a "preflight" request to the server hosting the cross-origin resource, in order to check that the server will permit the actual request. In that preflight, the browser sends headers that indicate the HTTP method and headers that will be used in the actual request.

> CORS (Cross-Origin Resource Sharing) is a system, consisting of transmitting HTTP headers, that determines whether browsers block frontend JavaScript code from accessing responses for cross-origin requests.

> Access-Control-Allow-Origin (CORS headers)
> Indicates whether the response can be shared.

> (crossorigin tag) Normal script elements pass minimal information to the window.onerror for scripts which do not pass the standard CORS checks. To allow error logging for sites which use a separate domain for static media, use this attribute. See CORS settings attributes for a more descriptive explanation of its valid arguments.

### What is diference between React and ReactDOM?

> React library is responsible for creating views(elements) and ReactDOM library is responsible to actually render UI in the browser.

### Can we do like this react.render(someComponent,document.querySelector('body'))?

> Yes, but it is not recommendable because body can be affected by some 3rd party libraries.

### What is difference between react.development.js and react.production.js files via CDN?

> Development versions are not suitable for production as production version is more minified and optimized.

### What is async and defer?

> Async -

> 1. The browser doesn’t block on async scripts (like defer).

> 2. Other scripts don’t wait for async scripts, and async scripts don’t wait for them.

> 3. DOMContentLoaded and async scripts don’t wait for each other:

> 4. async is used for independent third-party scripts, like counters or ads. And their relative execution order does not matter.

> 5. For module scripts, if the async attribute is present then the scripts and all their dependencies will be executed in the defer queue,

> 6. This attribute allows the elimination of parser-blocking JavaScript where the browser would have to load and evaluate scripts before continuing to parse. defer has a similar effect in this case.

> Defer -

> 1. Scripts with defer never block the page.

> 2. Scripts with defer always execute when the DOM is ready (but before DOMContentLoaded event).

> 3. Deferred scripts keep their relative order, just like regular scripts.

> 4. That may be important for cases when we need to load a JavaScript library and then a script that depends on it.

> 5. The defer attribute is ignored if the script tag has no src.

> 6. The defer attribute has no effect on module scripts — they defer by default.

> In async, browser while parsing and building the dom if accounts async then it downloads and execute the async script parallelly without blocking the dom

> In defer, browser while parsing and building the dom if accounts then it download them at that time but executes after the dom build completes.
