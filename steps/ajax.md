---
layout: default
---
# AJAX

## AJAX using jQuery

jQuery makes it easier to use Ajax by abstracting away the details of [XMLHttpRequest](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest).

To make an HTTP GET Ajax call using jQuery:

```javascript
  jQuery.get('/url/to/call', function(result){
    // Some code that uses result
  });
```

The result could be HTML or a Javascript Object (JSON). See some more details in the [jQuery.get() documentation](https://api.jquery.com/jquery.get/#jQuery-get-url-data-success-dataType).

For sending form data to the server side using AJAX one should use HTTP POST. The example below does an HTTP POST when a form with the id `fun-form` is submitted (usually by clicking a button).

```javascript
jQuery.submit('#fun-form', function(){

  jQuery.post('/url/to/post-to', {field1 : "one", field2 : "two"}, function(result){
    console.log(result)
  });

});
```

See more details about POST in the [jQuery.post() documentation](https://api.jquery.com/jQuery.post/#jQuery-post-url-data-success-dataType).

## Different styles

Ajax calls can return HTML that you then render on the client side. They can also return datasets in JSON or XML format which you can use on the client side to render data into the DOM.

Using HTML can be easier, but using datasets is a more flexible approach.

## Realities of AJAX

AJAX gives you much more flexibility, but makes your client side JavaScript more complicated: it moves some of the logic from the server side to the client side.

You can use [handlebars](http://handlebarsjs.com/) templating on the client side.
