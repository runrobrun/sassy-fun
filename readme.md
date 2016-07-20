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