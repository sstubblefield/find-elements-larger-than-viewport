# Find Elements Larger Than The Viewport

Just paste this guy in the developer console in your browser of choice, and hit Enter. If it does what it's supposed to, you should have a nice list of elements to punch in the face for being wider than they should be. Particularly great for mobile or responsive sites when you can't figure out why the page still scrolls sideways.

~~~
var docWidth = document.documentElement.offsetWidth;

[].forEach.call(
  document.querySelectorAll('*'),
  function(el) {
    if (el.offsetWidth > docWidth) {
      console.log(el);
    }
  }
);
~~~
