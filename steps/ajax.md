---
layout: default
---
# Create a more interactive experience

To create a more interactive web application you can take control of page rendering: rather than refreshing the whole page, you can refresh only certain fragments using the DOM and Ajax.

To do this you can use Ajax, which is based upon the `XMLHttpRequest` object. Ajax stands for **A**synchronous **Ja**vaScript and **X**ML, but people commonly use it to mean any asynchronous request from a web page. This allows you to send HTTP requests, such as GET and POST, to the backend asynchronously. See more details about `XMLHttpRequest` in [Chapter 17 of Eloquent JavaScript: HTTP](http://eloquentjavascript.net/17_http.html#xmlhttprequest).

The result of the request could be XML, JSON, script, text, or HTML. Most of the time the request will return HTML or a JavaScript Object (JSON). Using HTML can be easier, but using datasets is a more flexible approach.

The returned dataset can be used to render data into the DOM. You'll need to find things in the DOM, update them, maybe add or remove some classes. If you want a refresher on some of those ideas, have a look back at [Cape Town Green](http://taxi.projectcodex.co/)
and [Playing With Matches](http://matches.projectcodex.co/) and the code that you wrote for them.

Read more about [Ajax using jQuery](/steps/ajax-using-jquery.html) or see some alternatives on [You might not need jQuery](http://youmightnotneedjquery.com/#ajax).
