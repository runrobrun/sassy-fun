The watch command will watch for sass changes and automatically compile it upon saved changes

`sass --watch style.scss:style.css`

One time compilations can happen with the compile command.

`sass style.scss:style.css`

You can choose to display the compiled css in four ways:
:nested - Very easy to read should only be used in development
:expanded - Easy to read, does NOT contain the tab feature - should only be used in dev
:compact - Single line per rule any environment except production
:compressed - production only as it will be compressed and difficult to debug.


`sass --watch --style expanded style.scss:style.css`
`sass --style expanded style.scss:style.css`

Variables

Always start with $ and end with ;

Variables can point to other variables

Best used for colors, font stacks, widths, paddings, margins, other spacing etc.


Extend creates classes you would like to share attribues with. Any class that extends another
inherits it's attributes

.extendable-class {
    color: blue;
    font-weight:bold;
}

.big-blue {
    @extends .extendable-class;
    font-size:1.5em;
}

Mixins are functions that can take arguments

@mixin headline ($color, $size) {
  color: $color;
  font-size: $size;
}

h1 {
  @include headline(green, 12px);
}

nesting: SASS allows us to nest elements, classes, and ID's into parent/child collections
Typical rules is note to nest more than three levels deep