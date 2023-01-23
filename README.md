# SASS Framework

Set of designs which allow to build up themes quickly. Idea:

```SCSS
// Variation of designs
@use './designs/material';
@use './designs/flat';
@use './designs/flatter';


// Each design has unique customisation options
@use './designs/material' with (
    $color-primary: red,
    $color-primary: var(--red-color),
    $color-primary: map-get($colors, 'red');

    $media-mobile: 'only screen and (min-width: 300px)';
    $media-tablet: 'only screen and (min-width: 900px)';
);

// Then elements can be imported on their own
@use './element/button';
@use './element/input';
@use './element/image';

@use './layout/grid';
@use './layout/container';
```
