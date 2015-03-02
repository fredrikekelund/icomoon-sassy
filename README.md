# icomoon-sassy

> Two SASS mixins to make working with [IcoMoon](https://icomoon.io/) a little bit easer

Available via [Bower](http://bower.io/):
```sh
$ bower install icomoon-sassy
```

Get set up by including the main file in your SCSS with a simple:
```scss
@import "/path/to/bower_components/icomoon-sassy/icomoon";
```

## @include includeIcomoon("path")
Includes the IcoMoon fonts with the necessary @font-face rules. Takes an optional full path minus the file extension.

```scss
@include icomoonInclude("/path/to/icomoon");
```

## @include icomoonIcons((checkmark: "\e600"))
Creates classes for the class names and unicode points passed in a map. This is where you get the best of two worlds by combining the performance advantage of not using an attribute selector (like IcoMoon does by default) and the simplified development experience of not having to write out every class name manually.

```scss
@include icomoonIcons((
    checkmark: "\e600",
    close: "\e602",
    copy: "\e601"
));
```