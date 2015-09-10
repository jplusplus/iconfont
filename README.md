#Icons for J++

This repo contains a symbol font, for use across J++ projects. A few social media icons, and a J++ logo.

Fonts are generated using IcoMoon, and stored at Amazon S3, behind the Cloudfront CDN.

If you are going to use only one or a few icons, consider [Pirhoo's logo.js](https://github.com/Pirhoo/logo.js).

##Examples

    <link rel="stylesheet" type="text/css" href="example.css">
    
    Share on Facebook: <a href="https://www.facebook.com/sharer/sharer.php?u=http://jplusplus.se" class="fonticon">f</a>

    A J++-logo:
    <span class="fonticon jpluspluslogo">
        <span>j</span><span>+</span><span>+</span>
    </span>

Alternatively, you can use pseudo elements:

    It's a bird! <span class="twitter-icon"></span>

Either way, make sure that the content makes sense for people using screen readers, and for browsers that don't handle CSS fonts well.

##Glyphs

* `t`: Twitter logo
* `f`: Facebook logo
* `i`: LinkedIn logo
* `g`: Google+ logo
* `w`: WhatsApp logo
* `s`: Snapchat logo
* `j`: The 'j' of the J++ logo
* `+`: The '+' of the J++ logo

##CSS

The font can be either loaded from Amazon (pro: caching, con: extra http request), or embedded in the CSS (pro: no extra request, con: increased CSS size and no caching).

**From Amazon**

    @font-face {
        font-family: 'jplusplus';
        src:url('//static.jplusplus.se/iconfonts/jplusplus.eot?c2');
        src:url('//static.jplusplus.se/iconfonts/jplusplus.eot?#iefixc2') format('embedded-opentype'),
            url('//static.jplusplus.se/iconfonts/jplusplus.woff?c2') format('woff'),
            url('//static.jplusplus.se/iconfonts/jplusplus.ttf?c2') format('truetype'),
            url('//static.jplusplus.se/iconfonts/jplusplus.svg?c2#jplusplus') format('svg');
        font-weight: normal;
        font-style: normal;
    }

**Embedded**

    @font-face {
        font-family: 'jplusplus';
        src: url(data:application/x-font-ttf;charset=utf-8;base64,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) format('truetype');
        font-weight: normal;
        font-style: normal;
    }

##Implementation

It can be implemented with pseudo elements, or by actually printing letters in the markup. Either way, you'll have to take screenreaders and old browsers into considerations. Here are some boilerplates, trying to take accessability into account.

###Printing glyphs

**CSS**

    .fonticon {
        font-family: 'jplusplus';
        speak: none;
        font-style: normal;font-weight: normal;
        font-variant: normal;text-transform: none;
        line-height: 1;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
    }

**HTML**

    Share on Twitter <span class="fonticon" aria-label="Twitter logo" title="Twitter">t</span>

**Jade**

    p Share on Twitter
      span(aria-label="Twitter logo") t


###Pseaudo elements

**CSS**

    .twitter-icon:before {
        font-family: 'jplusplus';
        content: 't';
        speak: none;
        font-style: normal;font-weight: normal;
        font-variant: normal;text-transform: none;
        line-height: 1;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
    }
    .visuallyhidden { 
        position: absolute; 
        overflow: hidden; 
        clip: rect(0 0 0 0); 
        height: 1px; width: 1px; 
        margin: -1px; padding: 0; border: 0; 
    }

**HTML**

    Share on Twitter <span class="twitter-icon"></span><span class="visually-hidden">Twitter</span>

**Jade**

    p Share on Twitter
      span.twitter-icon t
      span.visually-hidden Twitter