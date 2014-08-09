# snap.svg.zpd

A zoom/pan/drag plugin for Snap.svg

This is an an adaptation of Andrea Leofreddi's [SVGPan library](https://code.google.com/p/svgpan/), version 1.2.2, for use as a [Snap.svg](http://snapsvg.io/) plugin.

This usually use on present view only. Not for Storing, modifying the paper.

[DEMO](http://huei90.github.io/snap.svg.zpd)

### Install

    $ bower install snap.svg.zpd --save

    $ npm install snap.svg.zpd --save

### Usage


Include `snap.svg.zpd.js` after `snap.svg.js`

```html
<script src="snap.svg.js"></script>
<script src="snap.svg.zpd.js"></script>
```

Writing the script

```js
var paper = Snap();
var bigCircle = paper.circle(150, 150, 100);
paper.zpd();

// with options and callback
paper.zpd(options, function (err, paper) {
    console.log(paper);
});

// with callback
paper.zpd(function (err, paper) {
    console.log(paper);
});
```

### options

#### zoom

    true or false: enable or disable panning (default true)

#### pad

    true or false: enable or disable zooming (default true)

#### drag

    true or false: enable or disable dragging (default false)

#### zoomScale

    number: Zoom sensitivity (default 0.2)

### More

#### zoomTo

```js
paper.zoomTo(1.5, 3000, mina.bounce, function (err, paper) {
    console.log(paper);
});
```
    zoom (must > 0), interval (ms optional), mina (optional), callback (optional)

#### paper.zpd('destroy')

```js
paper.zpd('destroy');
```
    Destroy all the zpd elements, events and nodes