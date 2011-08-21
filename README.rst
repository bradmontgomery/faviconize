jQuery Faviconize
-----------------

Faviconize (http://www.babylon-design.com/share/faviconize/)

Author: Samuel Le Morvan (http://www.babylon-design.com/)

A jQuery plugin for displaying a favicon on an external link.
Inspired Hyperlink Cues with Favicons of Ask the CSS Guy
Ask the CSS Guy (http://www.askthecssguy.com/2006/12/hyperlink_cues_with_favicons.html)

Examples
--------

For links like the following::

    <ul id="example"> 
    <li><a href="http://www.google.com/">Google</a></li> 
    <li><a href="http://www.yahoo.com/">Yahoo</a></li> 
    <li><a href="http://www.wikipedia.com/">Wikip&eacute;dia</a></li> 
    <li><a href="http://www.sitesansfavicon.tld/">Site sans favicon</a></li> 
    <li><a href="http://www.msn.com/">MSN</a></li> 
    </ul> 

Display the favicon before each link::

    $("ul#example a").faviconize({
        position: "before"
    });
    
Display the favicon after each link, and inlucde an default image for links without a favicon::

    $("ul#example a").faviconize({
        position: "after",
        defaultImage: "external.gif"
    });  

Make the favicon images clickable::

    $("ul#example a").faviconize({
        position: "before",
        defaultImage: "external.gif",
        linkable: true
    });

Give the favicon image a css class (so you can style it!)::

    $("ul#example a").faviconize({
        position: "before",
        defaultImage: "external.gif",
        linkable: true,
        className: "faviconize"
    });

Use an external default image, and provide exceptsions for certain links. These won't get a favicon displayed::

    $("ul#example a").faviconize({
        position: "before",
        defaultImage: "http://www.babylon-design.com/share/faviconize/external.gif",
        className: "faviconize",
        linkable: true,
        exceptions: ['http://www.msn.com/', 'http://www.ask.com']
    });

