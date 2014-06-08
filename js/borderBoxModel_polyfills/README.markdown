# Border-box model support for Internet Explorer 6-7

One of the new, shiny CSS3 proprieties that you can start using today is `box-sizing`.
This propriety allows you to switch between box models.

As of today, the browser support is really wide and this propriety works on:

- Firefox 1+ (with the `-moz` prefix)
- Safari 3+ (with the `-webkit` prefix)
- Opera 8.5+
- Internet Explorer 8+

This script will enable the `border-box` model also in IE6 and IE7 without trigger the *Quirks Mode*.

# Basic usage

The function has no dependency, just put the minified version of the script at the bottom of the page, before the `</body>`, so it will be lauched as soon as possible.
To be sure that it is executed only if the version of IE is prior to 8, use the conditional comments:

    <!--[if lt IE 8 ]>
    <script>
        var borderBoxModel = ...
    </script>
    <![endif]-->

# Known issues and limitations

- Currently it works only if padding and border are set in `px`.
- Width and height are written inline, so no fluid behaviour (es. onresize, min/max-width,...)
- Probably it needs more tests with complex layouts (with negative margins, ...)

# More info

Read my article about the [CSS3 box-sizing propriety](http://albertogasparin.it/)
