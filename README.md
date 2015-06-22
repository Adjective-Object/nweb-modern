#nweb-modern

nweb is a tiny static-page webserver from 
[IBM]((from http://www.ibm.com/developerworks/systems/library/es-nweb/) ).
I've made some minor convenience edits to make it usable for local testing / 
development.

### Changes since version 23

1. Allowed access for
    - svg, css, js, and map files
    - edited README.txt -> README.md and made the syntax markdown-compliant

### newb 23 readme:

1.  Bug fixed - was duplicating errors in the nweb.log file 
    - thanks to Kieran Grant for stopping this and pointing out the fix.
2. Added support for favicon.ico - if nothing elase this will stop annoying
    errors in the log file.  Most browsers on first encountering a webpage 
    also ask for this file.  The name mean favourite icon - Wikipedia has 
    more on this.  It is a tiny Bit Map image (normally called .bmp and 
    BMP editors can be used to create one - I used Windows Paint)
    I uses a very simple 16x16 pixels and 256 colour to keep the size and 
    complexity down.
    To add support I added .ico file extension to the allowed extensions 
    data structure and the sample favicon.ico file.
    This is then displyed by the browser at the little graphic next to 
    the URL. The one I made looks like this withe blue background.
    +---+
    |n  |
    |Web|
    +---+

3. As (1.) removed a few lines, I managed to add (2.) and still stay at 200 lines.

The code:
    nweb23.c -- the source code version 23
    client.c -- sample client end source code
