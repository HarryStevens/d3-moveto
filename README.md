# Deprecated

This module has been deprecated. Use [<i>selection</i>.raise()](https://github.com/d3/d3-selection#selection_raise) and [<i>selection</i>.lower()](https://github.com/d3/d3-selection#selection_lower) from [d3-selection](https://github.com/d3/d3-selection).

# d3-moveto

`d3-moveto` works with D3 selections to let you move SVG elements to the front or back of their parent SVG.

In interactive data visualizations, it is often necessary to bring elements to the front or back. But it is not easy to do this with SVG.

Unlike HTML elements, SVG elements have no `z-index` attribute, so it is impossible to make a younger sibling appear on top of an older one. Therefore, in SVG, elements which are appended to the DOM first will always appear on top of elements appended later. `d3-moveto` works by changing the order of elements in the DOM.

## Installing

If you use NPM, `npm install d3-moveto`. Otherwise, download the [latest release](https://github.com/HarryStevens/d3-moveto/tree/master/build). You can also load directly from [unpkg](https://unpkg.com/d3-moveto). You may use the entire [D3.js library](https://d3js.org/) or, at a minimum, [d3-selection](https://github.com/d3/d3-selection).

## Example

```html
<svg>
  <rect class="rect rect-1" x="0" y="0" height="10" width="10" fill="blue"></rect>
  <rect class="rect rect-2" x="10" y="0" height="10" width="10" fill="yellow"></rect>
  <rect class="rect rect-3" x="10" y="10" height="10" width="10" fill="green"></rect>
  <rect class="rect rect-4" x="0" y="10" height="10" width="10" fill="purple"></rect>
  <rect class="front" x="0" y="0" height="20" width="20" fill="red"></rect>
</svg>

<script src="https://d3js.org/d3-selection.v1.min.js"></script>
<script src="https://unpkg.com/d3-moveto"></script>
<script>
  var curr = 1;
  setInterval(function(){
    d3.selectAll(".rect").moveToBack();
    d3.select(".rect-" + curr).moveToFront();
    if (curr == 4) {
      curr = 1;
    } else {
      curr++;
    }
  }, 1000);
</script>
```

## API Reference

<a href="#moveToBack" name="moveToBack">#</a> <i>selection</i>.<b>moveToBack</b>()

Moves a selected SVG element to the back of the SVG.

<a href="#moveToFront" name="moveToFront">#</a> <i>selection</i>.<b>moveToFront</b>()

Moves a selected SVG element to the front of the SVG.
