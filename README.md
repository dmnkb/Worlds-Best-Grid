# Das weltbeste Grid 🚁
Das weltbeste Grid (world's best grid) is a wrapper of [mdc-layout-grid](https://github.com/material-components/material-components-web/tree/master/packages/mdc-layout-grid) and [include-media](https://github.com/eduardoboucas/include-media).

## Motivation
For a small project I recently decided to explore the implementation of Google's Material Design components. The markup implementation of [mdc-layout-grid](https://github.com/material-components/material-components-web/tree/master/packages/mdc-layout-grid) is quite straightforward, however I don't like the required classes ```mdc-layout-grid__cell``` (Well, I guess I just don't like BEM) and the lack of flexibility regarding custom breakpoints (Only ```desktop```, ```tablet``` and ```phone``` are supported). Therefore I used the SASS mixin implementation instead (```mdc-layout-grid($size, $margin, $max-width)```) and created my own classes: ```col s-12 m-6 l-4```. In order to be able to add custom breakpoints (such as "iPhone 12" for instance) I added [include-media](https://github.com/eduardoboucas/include-media). Please note that I limited the current availability to ```s``` (>0), ```m``` (>iphonex) and ```l``` (>ipad) for the sake of simplicity. This can easily be altered and extended to more semantic classes like ```iphone12``` and so on. And, of course, since all classes are created using SASS loops, adding custom classes is as simple as adding something like this to sass/app.scss:
```sass
@include media(">iphonex") {
  @for $i from 1 through 12 {
    &.m-#{$i} {
      @include mdc-layout-grid-cell('desktop', $i, 0)
    }
  }
}
```

## Install
#### NPM
```bash
npm install dasweltbestegrid
```
Or simply clone the GitHub repository.
Then, include the file in your project using an ```@import``` statement.

## License
This project is licensed under the terms of the [MIT license](https://github.com/eduardoboucas/include-media/blob/master/LICENSE.md).
