#flexless

A configurable set of LESS mixins that enables use of the CSS Flexible Box Layout Module [2012 Editor's Draft](http://dev.w3.org/csswg/css3-flexbox/) prefixed or un-prefixed with optional fallbacks for the [2009 W3C Working Draft](http://www.w3.org/TR/2009/WD-css3-flexbox-20090723/).

## Configuration

flexless supports 3 boolean configuration values that let you quickly drop support for either of the drafts or remove prefixes (if the spec is fully supported by the browsers you choose to support).

 * `@flexbox-compat`: Include Flexbox 2009 with prefixes
 * `@flexbox-prefix`: Include Flexbox 2012 with prefixes
 * `@flexbox-bare`: Include Flexbox 2012 without prefixes

## Usage

### Basic
Place the `flexbox/` folder in the same directly as your .less file and add the following line:
```
@import 'flexbox/flexbox.less';
```

### Custom
Define the configuration as desired, then import `flexbox/mixins.less` and/or `flexbox/classes.less`:
```
@flexbox-compat: false;    // Do not support Flexbox 2009 with prefixes
@flexbox-prefix: false;    // Do not support Flexbox 2012 with prefixes
@flexbox-bare: true;       // We only want to support Flexbox 2012 without prefixes

@import 'flexbox/mixins.less'; // We only need the mixins (no CSS classes)
```

## Mixins

The following mixins are provided:

* **.flex**  
Make a box into a flex box that will contain flex items.

* **.flex-direction(@direction)**  
Apply to flex boxes to set direction. Row arranges flex items horizontally, column arranges flex items vertically.  
@direction: `row`, `row-reverse`, `column`, `column-reverse`

* **.flex-ratio(@ratio)**  
Apply to flex items to set their span ratio, or how much of the available space they will take up.  
@ratio: Number

* **.flex-order(@order)** 
Apply to a flex item to set its order in the flex box, with the lowest order being displayed first.  
@order: Number

* **.flex-justify(@justify)**  
Apply to a flex box to set the same-axis alignment of its flex items.  
@justify: `flex-start`, `flex-end`, `center`, or `space-between`  
`space-around` is not supported for 2009 compatibility.

* **.flex-align(@align)**  
Apply to a flex box to set the cross-axis alignment of its flex items.  
@align: `flex-start`, `flex-end`, `center`, `stretch`, `baseline`

* **.flex-wrap(@wrap)**  
Apply to flex boxes to set wrapping  
@wrap: `nowrap`, `wrap`, `wrap-reverse`


## Classes
In addition to mixins, an optional set of classes are provided if you prefer to use CSS classes to define the behavior of your flexboxes.

* .flex

* .flex-justify-start

* .flex-justify-end

* .flex-justify-center

* .flex-justify-end

* .flex-align-start

* .flex-align-end

* .flex-align-center

* .flex-align-stretch

* .flex-align-baseline

* .flex-direction-row

* .flex-direction-row-rev

* .flex-direction-column

* .flex-direction-column-rev

* .flex-wrap

* .flex-nowrap

* .flex-wrap-reverse

* .flex-ratio-1

* .flex-ratio-2

* .flex-ratio-3

* .flex-ratio-4

* .flex-ratio-5

* .flex-ratio-6

* .flex-ratio-7

* .flex-ratio-8

* .flex-ratio-9

* .flex-ratio-10

* .flex-order-1

* .flex-order-2

* .flex-order-3

* .flex-order-4

* .flex-order-5

* .flex-order-6

* .flex-order-7

* .flex-order-8

* .flex-order-9

* .flex-order-10
