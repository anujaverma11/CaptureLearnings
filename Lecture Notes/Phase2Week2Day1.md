variables
if you don't put var it will always be a gobal variable
var myVariable = "test"
==============================================================
strings

==============================================================
What's false?
if(false) {
  console.log("that wasn't false")
}

[], 0, '' , null, undefined, NaN - all will return falsy value
=====================================================================
functions
===========
anything having () after it, JS will try to run it.

var myFunction = function(){}
==============================================================

Object literals!
================
var shoe =
{
  type: "Vans"
  walk: function()
  {console.log ("stop that shoe!")}
}

shoe.walk()


var createCar = function()
{
  var car=
  {
  milesDriven: 0,
  drive: function(){
  console.log("walk drive walk");
  this.milesdriven +=5
}
  } return car;
}

var buick = createCar();
buick.milesdriven
buick.drive()

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
jsbin.com/catibu/6/edit?js,console

drive is an anonymous function (if it defined without a name)
var a = new object();
a.drive = function(){
  console.log("walk drive walk");
  this.milesdriven +=5
}

a.drive();

gist stujo oojs

====================
Factory Function - can we use manufacture without this??
====================

bind --- ??
bind my funtion with event handler

All constructor method should start with a uppercase.

var Vehicle = function (manufacturer){}
new creates a new object and

private properties are defined by _ underscore. _manufacturer

prototype is a property of all functions in Java Script.


purecss.io/menus/

