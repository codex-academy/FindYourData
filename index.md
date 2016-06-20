---
layout: default
---

# Find my data

Once your system has data, the users will want to find particular things. The easier you make it to find things, the better your system will be. This is especially important as the amount data in your system increases.

Users that are searching for information might not know exactly what they are looking for so our search functionality should allow for partial matching when searching for data.

First you'll make a regular search using an HTML form, the POST method, and SQL Database queries. Then you'll enhance it using Ajax.

## Search bar

Add a search bar to your products screen. Users will type the product name in a text field and then press the search button. The products that match their search should be displayed.

## Interactive search bar

Let's add an interactive search bar to your Products screen.

The search bar should:

* automatically start searching after you have typed 3 characters;
* display matches for both Product and Category names;
* display all products if the search bar is empty.
