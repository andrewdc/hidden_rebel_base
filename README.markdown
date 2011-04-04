And now, your highness, we will discuss the location of your _hidden_rebel_base.sass
=======================

Well, what can I say. I use StaticMatic to generate rapid UI prototypes and every-time I start a new one I find myself having to re-do my _base.sass partial file, or paste it from a previous project. Hunting around for it gets kind of annoying. 

It makes more sense to put this file in Git so that I can keep it updated and pull/push it from a public source. Feel free to fork this, add, steal - whatever you would like!

*Note*: I altered the deal, by renaming `_base.sass` to `_hidden_rebel_base.sass` so you won't stomp an exsisting `_base.sass` file...Pray I don't alter it further.

-Adc

## Setup

1. Simply lock tractor beams on this _hidden_rebel_bass.sass repo and pull into your `/src/stylesheets`. Usually the same dir/ as your main project SASS file.

     `git clone git://github.com/andrewdc/hidden_rebel_base.git`

2. Add `@import "hidden_rebel_base/_hidden_rebel_bass.sass"` to the head of your working SASS file. If you don't put this file elsewhere,simply point to the file e.g. 

     `@import "theyre/on/dantoine/_hidden_rebel_base.sass"`
         
## Documentation

### Clearfix

Applies to the :after psuedo-class so you know, watch your back on this one a little with a certain browser, but you won't have to add this to a psuedo-class

     @include clearfix

### Truncate String with ...

Simple - just set the width variable to whatever you want the cutoff to be. Firefox doesn't support this though, so feel free to complain to Mozilla. Default `width = 100px`

    @include truncate(width)     
     
### Linear Gradiant + Background image (optional)

Start with top color and go to bottom color. If you want an image over top, add this in with any or all of the full `background:url() repeat x-pos y-pos;`. This is optional, so not providing the third argument won't do a ruttin' thang!

    @include lin-grad(top-color, bottom-color, optional-second-background)

### Image Replacement

Like you might guess, Swap out some html and replace it with an image. 

    @include img_replace(../to/the/image, width, height)   
    
### Border Radius

This one allows you to set a radii for each corner starting Top-Left and going clockwise

	@include borderRadius(topleft, topright, bottomright, bottomleft)  

### Box Shadow

I have a simple implimentation of the box shadow in this file:

		@include boxShadow( $x: 5px,$y: 5px, $blur: 5px,$color: #000)

At current, I recommend using the mixin from [Compass](http://compass-style.org/docs/reference/compass/css3/box_shadow/) for this. It supports the optional `inset` value. In fact - if you are familiar with Compass, you can always use it instead of The Hidden Rebel Base. (Of course, I will find your lack of faith: Disturbing.) It has a much more robust application of many of these mixins. However, does it have the cool name? No...

	@include box-shadow($color, $hoff, $voff, $blur, $spread, $inset)
	 
Like I said - Check out [Compass](http://compass-style.org/) if you aren't familiar with it. It does everything that HRB does, times a million. 

Mad props to [Chris Eppstein](http://chriseppstein.github.com/)!

## I want CSS3 in Internet Explorer...NOT EXCUSES!!!!

Oh - fellow designer...hidden_rebel_base has your back, sorta...

Support for CSS3PIE

I added a couple modifications to some of these mixins so that they properly function with a sweet behaviour file for older versions of Internet Explorer that allow it to handle some CSS3 stuff. You can grab this file at [CSS3PIE](http://css3pie.com/). For a demonstration/test, try opening this in IE: [Pure CSS3 OSX Window](http://dl.dropbox.com/u/3153617/interfaces/spice/site/index.html) 
      
## Hey!?!? What's the deal with the indenting?

...Yes, I use the older indented sass syntax. That is because it pwnes the face off the newer syntax. But that's just me. Sorry for the inconvenience if you roll with the newer scss. Perhaps I'll whip together a scss version of these in the future. Bug me about it... ;)

For the record - with the old syntax, feel free to use:

		+mixinName(properties)



