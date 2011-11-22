=================
jquery.fb-wall.js
=================

This is an extension of the excellent fb.wall jQuery plugin by Neosmart.  For the
original, see::

    http://www.neosmart.de/social-media/facebook-wall

This extension adds the following plugins:

    ``fbLikes``: shows likes for a Facebook object.
  
    ``fbComments``: shows comments for a Facebook object.

It's rough around the edges at the moment; apologies.

Usage
-----

``fbLikes``

    The following is the easiest way to render likes for a given Facebook object
    into a container with id "container"::

        $('#container').fbLikes({
            id: "some object id",
            accessToken: "your application's access token",
        });

    In addion, the following options can be specified:

        ``userId``:
             the id of the Facebook user you are rendering this for (so that
             it shows "you like this" and so on).

        ``formatDate``:
             a function that takes a string representation of a date (when the
             comment was posted) and returns a formatted version of it.
        
Example
-------

To run the provided example, run the following from within the same directory as this
README, and then visit `http://localhost/example.html`_::

    python -m SimpleHTTPServer
