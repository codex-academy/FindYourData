---
layout: default
---
# AJAX

## AJAX using jQuery

JQuery makes it easier to use AJAX by abstracting away the details of XMLHttpRequest.

To make a HTTP GET Ajax call using jQuery:

```javascript
  jQuery.get('/url/to/call', function(result){
    // display the results of the call in a DIV
    document.getElementById('targetDiv').innerHTML = result;
    //or use jQuery
    //jQuery('#targetDiv').html(result);

  });
```

alternatively the call can return a Javascript Object (JSON):

```javascript
  jQuery.get('/url/to/call', function(result){
    // display the results of the call in a DIV

    var products = result.products;

    // loop through the products...
    products.forEach(function(product){
      //we just display the product to the console.
      console.log(product.name)  
    });
  });
```

See some more details in the [jQuery.get() documentation](https://api.jquery.com/jquery.get/#jQuery-get-url-data-success-dataType)

For sending form data to the server side using AJAX one should use HTTP POST.

The example below will do a HTTP POST when a button is clicked.

```javascript
jQuery.click('#submitForm', function(){

  jQuery.post('/url/to/post-to', {field1 : "one", field2 : "two"}, function(result){
    console.log(result)
  });

});
```

See more details about POST in the [jQuery.post() documentation](https://api.jquery.com/jQuery.post/#jQuery-post-url-data-success-dataType).

## Different styles

Ajax calls can either return sections of HTML that you can render on the client side or it can return some datasets in JSON or XML format which one can use on the client side to render data into the DOM.

Using the HTML sections is easier to use, but using the returned datasets is a more flexible approach.

## Realities of AJAX

AJAX gives you much more flexibility, but makes your client side javascript more complicated. As it moves some of the logic from the server side to the client side.

> Good news : you can use [handlebars](http://handlebarsjs.com/) templating on the client side.
