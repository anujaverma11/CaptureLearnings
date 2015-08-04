## Phase 2 Week2 Day 2
### Closure

- function that keeps reference
- Variable from its parent scope


```
function setlocation(city){
  var country = "france";

  function setcity(){
    console.log("You are in" + city + " " +country);
  }
  return setcity
}

var output = setlocation("paris");
output()
```


- allows you to keep the scope together.

```
function citylocation(){
  var city = "paris";

  return {
      get: function() {console.log(city);},
      set: function(newCity) {city = newCity}
  };

}
var myLocation = citylocation();
myLocation.get()
myLocation.set("munic");
myLocation.get()

```
closure are big part of Javascript.

### Callbacks
In Javascript you can pass a function as a parameter.
Callback is the function or argument passed into another high order function.
```
function citylocation() {
  city = "Paris";
  return city;

}

function countrylocation(citylocation) //citylocation parameter
  {country = "France"
  console.log("You are in" + city + " " +country);}


  countrylocation(citylocation()); //citylocation argument
```

Countrylocation is highorder
Citylocation is callback function.
The above program return "You are in Paris France"


Another way to call callback function inside higorder

```
function citylocation() {
  city = "Paris";
  return city;

}

function countrylocation(citylocation)
  {country = "France";
  citylocation();
  console.log("You are in " + city + " " +country);}

  countrylocation(citylocation);
```







