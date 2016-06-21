---
layout: default
---

# Ajax using jQuery

You can use jQuery to abstract away the details of [XMLHttpRequest](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest). Including jQuery in your app comes with a cost as well as a benefit. You can read a little more about this on [the JavaScript page of the Front-end Field Guide](http://fefg.projectcodex.co/javascript.html), and a broader discussion of frameworks and libraries at [Front-end Field Guides](http://fef.projectcodex.co/).

To make an HTTP GET Ajax call using jQuery:

```javascript
  jQuery.get('/url/to/call', function(result){
    // Some code that uses result
  });
```

You can read more about this in the [jQuery.get() documentation](https://api.jquery.com/jquery.get/#jQuery-get-url-data-success-dataType).

For sending form data to the server side using Ajax you should use HTTP POST. The example below does an HTTP POST when a form with the id `search` is submitted (usually by clicking a button). Note that you need to get the data from the form (here we use jQuery and it's `val()` method)

```javascript
jQuery('#search-form').submit( function(event){

  // Stop the form from submitting normally
  event.preventDefault();

  // Get the search term from the DOM
  var theSearchTerm = jQuery('#search-term').val();

  // use jQuery to POST the data to the /search URL
  jQuery.post('/search', {searchterm: theSearchTerm}, function(result){
    console.log(result);
  });

});
```

See more details about POST in the [jQuery.post() documentation](https://api.jquery.com/jQuery.post/#jQuery-post-url-data-success-dataType).

## Realities of Ajax

Ajax gives you much more flexibility, but makes your client side JavaScript more complicated: it moves some of the logic from the server side to the client side.

You can use [Handlebars](http://handlebarsjs.com/) templating on the client side.
