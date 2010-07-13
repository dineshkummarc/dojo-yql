= About

This is a Dojo interface to Yahoo's [YQL][yql].  It's based on Dav Glass's
[yui-yql][yui-yql], mostly rewritten around dojo.io.script

To use it:

    dojox.yql("SELECT * from friendfeed.feeds WHERE nickname = 'slackorama'", { 
        load: function(data){
            console.dir( data );
        },
        error: function( e ) {
            console.error( e );
        }
     });

Or more traditionally as you would a Ajax request, or any other dojo.Deferred:

    dojox.yql("select * from internet")
        .addCallback(function(data){ })
        .addErrback(function(error){ })
    ;

== Note

If you are using this module, you must comply with Yahoo's [usage and
attribution requirements][usage].

== TODO:

 *   Tests (fork/port is wholly untested)
 *   Documentation (inline docs added, though could be expanded)
 *   Profit (not likely)

[yql]: http://developer.yahoo.com/yql/
[yui-yql]: http://github.com/davglass/yui-yql/
[usage]: http://developer.yahoo.com/faq/#token
