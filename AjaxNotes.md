### AJAX (Asynchronus Java Script and XML)
- send request dynamically

$(document).ready(function(){
  bindListeners()
})
var bindListeners = function(){
  $('a').on('click', function(e){
    e.preventDefault() //Sending the request and asking not to do the default

    $.ajax({
      url: '/animals'
      }).done(function(response){
        console.log(response)
        })
})console.log("Funkytown")
}

- .done will make sure previous function is finished before it recevies response.
- AJAX is asynchronous because ajax request run parallel with other code in the window.
- FunkyTown will print before we receive the response.

Reference: jquery ajax documentation
========================================================================

```
var bindListners = function(){
  $('a').on('click', function(e){
  e.preventDefault()
  getform()
 })
}

var appendform() = function(response){
  $('#formTarget').append(response)
}

var hideLink() = function(){
$('a').hide()
}


var getform = function(){
  $.ajax({
    url:'/form'
  }).done(function(any_response_variable){
  appendForm(form)
  hideLink()
  })
}
```

### Event Delegation
================

```
var bindListners = function(){
  $('a').on('click', function(e){
  e.preventDefault()
  getform()
})
  $('#formTarget').on('submit', 'form', function(){
  e.preventDefault()
  var $(this).serialize()
})

}

var appendform() = function(response){
  $('#formTarget').append(response)
}

var hideLink() = function(){
$('a').hide()
}

var postForm = function(data){
  $.ajax({
    method: 'POST',
    url:'/appointments'
    data: data,
    dataType: 'JSON'
  }).done(function(response){
  appendappointment(response)
})
}

var appendAppointment = function(data){
  $('#appointments').append('<h2>' + data.name + '</h2>')
  $('#appointments').append('<h2>' + data.date + '</h2>')
}

var getform = function(){
  $.ajax({
    url:'/form'
  }).done(function(any_response_variable){
  appendForm(form)
  hideLink()
  })
}

```
In Controller =>
'/post'
app.to_json

We are expecting a JSON type of data






