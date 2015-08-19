
Atomic Css resource
jkymarsh/nuclide#
========================================================================
.html

<html>
<head>
  <title></title>
  <link rel="stylesheet" href=""style.css>
</head>
<body>
  <div class="sample"
</body>
</html>

.css
// box-sizing from css tricks
html {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
*, *:before, *:after {
  -webkit-box-sizing: inherit;
  -moz-box-sizing: inherit;
  box-sizing: inherit;
  }

.sample {
  width: 200px;
  padding: 20px;
  border: 1px solid red;

}

.sample:after{content:something}

.debug {
  border: 1px solid red;
}

========================================================================

//display something after content in sample.
//css tricks css box-sizing
*  on line 24 means everything
use clearfix for floats

cross browser testing
======================


debug class

Floats
========================================================================
<html>
<head>
  <title></title>
</head>
<body>

</body>
</html>



.fl-l{float: left;} //define float left class
.fl-r{float: right;}

google css clearfix

.clearfix:after {
   content: ".";
   visibility: hidden;
   display: block;
   height: 0;
   clear: both;
}


========================================================================
positioning
  absolute
  relative
  static default

.pos-a {position: absolute;} // child positioned as absolute.
.t-0 {top: 0;}
.l-0 {left: 0;}
.pos-r {position: relative;} //parent has to be relative
.pos-f {position: fixed;}


fixed positioning does not work with

inline-block
.d-ib{disply: inline-block;}
.ta-c{;}


CSS Tools
Nuclide-ui
grid
resetter reset css
normalize css
hack-design
P3 pixel production some book


www.responsive.gs


{margin: 0 auto} //centralize everything
