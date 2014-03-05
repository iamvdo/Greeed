Greeed
======

Greeed is a minimalist (only 2.9K minified), responsive JS-based grid layout. **The goal is to display items on columns (based on media-queries), where items are presented from top to bottom, regardless of the number of columns.**

No CSS layout can do that, even Flexbox! :(

See it in action using [Heeere](https://github.com/iamvdo/Heeere), CSS3D Transforms and transitions [in my personal website](http://iamvdo.me)

## Usage

You need to bind greeed, with 2 parameters:

* A DOM selector targeting the parent containing items (The Greeed)
* Options

```javascript
// Bind
greeed.bind('.Greeed', {
	breakpoints: [34,48,65,88,110,140]
	}
);

```

## Options:

* `breakpoints` (required): an array with all breakpoints. Each breakpoints must be in `em` unit and represent how many columns you want between 2 breakpoints. In the example above, there will be 1 column from 0 to 34em, then 2 columns from 34em to 48em, and so on...
* `classColumn`: the `class` added to each column created (`li` elements). Default `.Greeed-column`.
* `classColumnInner`: the `class` added to each inner column created (`ul` elements). Default `.Greeed-column-inner`.
* `classItem`: the `class` added to each elements of the Greeed (`li` elements). Default `.Greeed-item`.
* `classFakeItem`: the `class` added to each fake elements created in order to make each columns the same height (see nex option). Default `.Greeed-item--fake`.
* `fakeItem`: boolean making each columns the same height or not, by creating a fake item. Default `true`.
* `afterInit`: a callback function called after first initialization
* `afterLayout`: a callback function called after every new layout calculation (browser's window resize, new orientation, etc.)
