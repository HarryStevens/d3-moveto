# d3-moveto

`d3-moveto` works with D3 selections to let you move SVG elements to the front or back of their parent SVG.

In interactive data visualizations, it is often necessary to bring elements to the front or back. But it is not easy to do this with SVG.

Unlike HTML elements, SVG elements have no `z-index` attribute, so it is impossible to make a younger sibling appear on top of an older one. Therefore, in SVG, elements which are appended to the DOM first will always appear on top of elements appended later.

## Installing

If you use NPM, `npm install d3-moveto`. Otherwise, download the [latest release](https://github.com/harrystevens/d3-moveto/releases/latest).

## API Reference

<a href="#moveToBack" name="moveToBack">#</a> <i>selection</i>.<b>moveToBack</b>()

Moves a selected SVG element to the back of the SVG.

<a href="#moveToFront" name="moveToFront">#</a> <i>selection</i>.<b>moveToFront</b>()

Moves a selected SVG element to the front of the SVG.