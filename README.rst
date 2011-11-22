=================
jquery.fb-wall.js
=================

This is an extension of the excellent fb.wall jQuery plugin by Neosmart.  For the
original, see::

    http://www.neosmart.de/social-media/facebook-wall

This extension adds the following plugins:

    ``fbLikes``: shows likes for a Facebook object.
  
    ``fbComments``: shows comments for a Facebook object.

To see these two additional plugins in action, visit::

    http://zachsnow.com/demos/jquery-fb-wall/

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

    In addition, the following options can be specified:

        ``userId``:
            the id of the Facebook user you are rendering this for (so that
            it shows "you like this" and so on).


``fbComments``

    This plugin shows Facebook comments for a given Facebook object, adding them
    to a container with id "container"::

        $('#container').fbComments({
            id: "some object id",
            accessToken: "your really elaborate access token"
        });

    Along with the some options mentioned for ``fbLikes``, the following options
    are allowed:

        ``formatDate``:
            a function that takes a string representation of a date (when the
            comment was posted) and returns a formatted version of it; for
            instance, to get a common US format, you might use the following::

                $('#container').fbComments({
                    ...,
                    formatDate: function(s){
                        var date = new Date(s);
                        var month = date.getMonth() + 1;
                        var day = date.getDay();
                        var year = date.getFullYear();
                        return month + '/' + day + '/' + year;
                    }
                })

        
Example
-------

To run the provided example, run the following from within the same directory as this
README, and then visit `http://localhost:8000/example.html`_::

    python -m SimpleHTTPServer

This assumes, of course, that you have `Python <http://python.org>`_ installed.
