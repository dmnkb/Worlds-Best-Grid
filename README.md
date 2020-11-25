# Das weltbeste Grid 🚁
Das weltbeste Grid (world's best grid) is a mobile-first lightweight and easy-to-use 12 columns responsive grid that covers breakpoints for most of currently common mobile devices. Under the hood it makes use of [mdc-layout-grid](https://github.com/material-components/material-components-web/tree/master/packages/mdc-layout-grid) and [include-media](https://github.com/eduardoboucas/include-media).

## Motivation
Most responsive frameworks I used to work with have a couple of things in common: Limited amount of breakpoints (```small, medium, large```), complex classes (```mdc-layout-grid__cell```) and an unnecessary overhead.

## Solution
Using SASS loops in combination with [include-media](https://github.com/eduardoboucas/include-media) all breakpoint classes are generated procedurally. Adding new breakpoints is as easy as extending the ```$breakpoints``` list.

## Example
Say, you want a container to fill 9 / 12 columns when the user is using an iPhone 12:
```html
<div class="grid">
  <div class="inner">
    <div class="col ip12-9">
      Content goes here
    </div>
  </div>
</div>
```
See? Simple.

## Available breakpoints
```
$breakpoints: (
  small: (
    "size": 0px,
    "class": "s"
  ),
  medium: (
    "size": 640px,
    "class": "m"
   ),
  large: (
    "size": 1024px,
    "class": "l"
  ),
  xlarge: (
    "size": 1200px,
    "class": "xl"
  ),
  xxlarge: (
    "size": 1440px,
    "class": "xxl"
  ),
  iphone5: (
    "size": 320px,
    "class": "ip5"
  ),
  iphonex: (
    "size": 375px,
    "class": "ipx"
  ),
  iphone11: (
    "size": 414px,
    "class": "ip11"
  ),
  iphone12: (
    "size": 390px,
    "class": "ip12"
  ),
  ipad: (
    "size": 810px,
    "class": "ipad"
  ),
  redmi-note-8: (
    "size": 1080px,
    "class": "rn8"
  ),
  galaxy-a51: (
    "size": 1080px,
    "class": "ga51"
  )
);
```

## Custom breakpoints
In order to add custom breakpoints simply clone this project and extend the breakpoint list inside ```sass/app.scss```.

## Install
#### NPM
```bash
npm install dasweltbestegrid
```
Or simply clone the GitHub repository.
Then, include the file in your project using an ```@import``` statement.

## License
This project is licensed under the terms of the [MIT license](https://github.com/eduardoboucas/include-media/blob/master/LICENSE.md).
