## Phase 2 Week2 Day 3
Event Handler Review
Callbacks with event handler
bind

```
var color = "#fff"

var Changer = function(){
  this.buttons = document.querySelectorAll(".button-container button")
}

var changer = new Changer();

for (i=0, i< changer.buttons.length; i++){
changer.buttons[i].addEventListener("mouseover", function(e)){
  this.style.backgroundColor = color
  }
}

document.querSelector('#change').addEventListner("click",function(){
  color = '#ff0000'
})
```


