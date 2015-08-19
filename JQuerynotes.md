### JQuery notes
JQuery is saved with "filename.js"

#### To include the .js file in HTML
Include the following code in head tag of HTML file
```
<script type="text/javascript" src="script.js"></script>
```

### Start up writing jquery

$(document).ready(function(){});

.ready is a signal where page says DOM is finished loading. We only want our JQuery code to trigger once DOM triggers ready.

- Putting document between the parentheses refers to the HTML document itself.
- .ready(); is a function, or basic action, in jQuery. Whatever goes in .ready()'s parentheses is the jQuery event that occurs as soon as the HTML document is ready.
- Functions are the basic unit of doing work in jQuery.

#### Where to add the JQuery script?
Load JQuery in your HTML
<script src="jQuery.min.js"> </script>
<script src="yourfile.js"> </script>


```
<h1>Where do you want to go?</h1>
<h2>Travel Destinations</h2>
<p>Plan your next adventure</p>
<ul id="destinations"



```



### DOM (Document Pbject Model)
DOM is a tree like structure created by browsers so we can quickly find HTMLelements using JS.

Inorder to interact with DOM all browsers use JS.

We need to make sure the DOM is finished loading before we use any JQuery on the page.

#### To change an element
```
$("h1").text("Where to?")
```
Will change heading text to "Where to?"

#### JQuery program structure
```
$(document).ready(
function(){
<!-- all code goes here -->
}
);
```
#### To select an ID from HTML page

```
$('#id_name')
```


#### To select a class from HTML page

```
$('.class_name')
```


<li class="vacation america"> means that there are two classes for that element: .vacation and .america.
```
$('.america')
```
will just select elements having america class.

#### Descendent Selector

$('#destinations li')

parent is destination, li is descendents. (All descendents)

#### Select immediate children of an element (Using Child selector)

$('#destinations > li')

parent is destination, li is descendents. (All direct descendents)

#### Selecting Multiple items
$("#destination, .promo")


#### Pseudo Selector

#("destinations li:first")
#("destinations li:last")
#("destinations li:even")
#("destinations li:odd")

## Traversing the DOM

$('#destinations').find('li').last();
$("#vacations").find("li").last();

- Using find with DOM item

Traversing takes a little more time but its faster.


#### Walking the DOM

$('li').first().next().prev();

This is called method chaining.

#### Walking up the DOM

$('li').first().parent();

#### Walking down the DOM

$('#destinations').children("li");

Will select only direct descendents.


#### Appending to the DOM

Create a new paragraph.

```
$(document).ready(function(){
  var price=$('<p>From $399.99</p>')
  $('.vacation').appand(price);
  $('button').remove();
});


```

.append(<variable>)
.prepend(<variable>)
.after(<variable>)
.before(<variable>)

Some people think the below command are more readable.

variable.prependTo(<element>)
variable.appendTo(<element>)
variable.insertAfter(<element>)
variable.insertBefore(<element>)

### Acting on Interactions

We use .on method

.on(<event>,<event handler>)


### Refactoring Using Interaction

$(this).remove();

$(this).closest('.vacation').append(price);

### Traversing and Filtering

$(document).ready(function(){
  $('button').on('click', function(){
    var vacation = $(this).closest('.vacation');
    var amount = vacation.data('price');
    var price = $('<p>FROM $'+amount+'</p>');
    vacation.append(price);
    $(this).remove();
  })
})

### Filters
$('$filters').on('click', '.onsale-filter', function(){
  $('.highlighted').removeclass('.highlighted');
  $('.vacation').filter('.onsale').addClass('.highlighted');
})


