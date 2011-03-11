Hidden Rebel _Base.sass
=======================

Well, what can I say. I use StaticMatic to generate rapid UI prototypes and every-time I start a new one I find myself having to re-do my _base.sass partial file, or paste it from a previous project. Hunting around for it gets kind of annoying. 

It makes more sense to put this file in Git so that I can keep it updated and pull/push it from a public source. Feel free to fork this, add, steal - whatever you would like!

-Adc

## Setup ##

1. Simply pull down this _bass.sass file into your project. Usually the same dir/ as your main project SASS file.
'git checkout git@github.com:andrewdc/hidden_rebel_base.git'

2. Add @import "\_base" to the head of your working SASS file. If you don't put this in the same folder, then simply point to the file e.g. 

`@import "theyre/on/dantoine/_bass.sass"`

Documentation
-------------

#### Clearfix

Applies to the :after psuedo-class so you know, watch your back on this one a little with a certain browser.

     @mixin clearfix
     
     
#### Linear Gradiant + Background image (optional)

Start with top color and go to bottom color. If you want an image over top, add this in with any or all of the full `background:url() repeat x-pos y-pos;`. This is optional, so not providing the third argument won't do a ruttin' thang!

    @mixin lin-grad($from, $to, $bga: url())
    

Ps. And yes, I use the old indented sass syntax. It just works for me. Sorry for the inconvenience if you roll with the newer scss. Perhaps I'll whip together a scss version of these in the future. Bug me about it... ;)