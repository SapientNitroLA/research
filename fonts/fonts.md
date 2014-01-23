<link rel="stylesheet" type="text/css" href="../../../../library/css/global/main.css" media="screen" />

# Fonts #

### Contents ###

1. [Browser Formats](#broswer-formats)
2. [Font Face](#font-face)
3. [Served Fonts vs. Self Hosted](#served-and-self-hosted)
4. [Quirks](#quirks)
5. [References](#references)

## Browser Formats ##

Different browsers require different font formats:

* Internet Explorer: `EOT`
* Mozilla: `OTF` `TTF`
* Safari + Opera: `OTF` `TTF` `SVG`
* Chrome: `TTF` `SVG`
* Mobile broswers: `SVG`

## Font Face ##

Use the following declaration:

    @font-face {
        font-family: 'open_sansbold';
        src: url('opensans-bold-webfont.eot');
        src: url('opensans-bold-webfont.eot?#iefix') format('embedded-opentype'),
             url('opensans-bold-webfont.woff') format('woff'),
             url('opensans-bold-webfont.ttf') format('truetype'),
             url('opensans-bold-webfont.svg#open_sansbold') format('svg');
        font-weight: normal;
        font-style: normal;
      
    }

***Supported in***

* IE 4+
* Firefox 3.5+
* Safari 3.1+
* Opera 10+
* Chrome 4+

## Served and Self Hosted ##

### Hosting Service ###


1. Wider selection of fonts
2. Spreading http requests across third party server = improves performance
3. Files from third party can (possibly) be cached already by users

Web hosting: Pay as you go, 250k page views with notifications at 75%, 90% etc. `$29/250k pageviews`

Server hosting: @ 290.00/year per font (~8 fonts currently being used) `$2320/year`

3rd parties: [Typekit](https://typekit.com/), [Fontdeck](http://fontdeck.com), [Edge Fonts](http://edgefonts.com)

### Self Hosting ###

1. Faster font rendering (most of the time)
2. No dependency on provider's up time
3. No subscription fees or page view limitations
4. No JS dependency for font delivery

## Quirks ##

**Unstyled Text Flash**

Happens before a font face is loaded. Example fixes:

[Web Font Loader](http://code.google.com/apis/webfonts/docs/webfont_loader.html)

[Prevent Performance Hit](http://css-tricks.com/preventing-the-performance-hit-from-custom-fonts/)


## References ##

[font-face Kit Generator](http://www.fontsquirrel.com/tools/webfont-generator)

[Web Fonts @ html5 rocks](http://www.html5rocks.com/en/tutorials/webfonts/quick/)

[Font Face @ webtuts](http://webdesign.tutsplus.com/articles/typography-articles/figuring-out-font-face/)


   
