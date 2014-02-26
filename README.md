jProcessingJS
=============

A lightweight easy-to-use ProcessinJS extension, for advanced sketch integration in your webdesign...

### Why ?

Because ProcessingJS is a great tool to display a Processing sketch online, and it's a great html5 IDE too.  
But when it comes to integrate a sketch in a complex webdesign, it can become really painful.  
**A processingJS sketch is not responsive at all, nor will it display fullscreen, and just put an html overlay above it and you'll lose all mouse/touch inputs.**  
You may find solutions for all that online, but what if you could do it all with **only one Javascript line, directly in your sketch** ?

### What ?

**jProcessingJS** is a **lightweight Javascript library** (3.64 Ko minified), that extends the default ProcessingJS behaviours.  
It come as a ProcessingJS extension, and allows you to easily :

  * make your sketch **fullscreen**
  * make your sketch **responsive**
  * keep **mouse/touch interactions** even with an **html overlay**
  * optimise some Math methods (as done by [jspeed](http://code.google.com/p/jspeed/))

### How ?

Just place **jprocessingjs.min.js** next to the official **processing.js** lib, and import it in your html header as usual.  
Then you'll have access to **a new method that replaces the size() method in your sketch's setup()**.

**For a fullscreen sketch** just write in your sketch's setup() :

    jProcessingJS(this, {fullscreen:true});

**For a responsive sketch**, replace the size() instruction with :

    jProcessingJS(this); // responsive is the default behaviour

then you might scale your sketch using CSS targeted to your canvas (width:100% for exemple).

To enable **mouse/touch interaction even with an html overlay** above your sketch :

    jProcessingJS(this, {mouseoverlay:true});
    
Of course you may mix several parameters :

    jProcessingJS(this, {fullscreen:true, mouseoverlay:true});
    
will give you a **fullscreen responsive sketch, with mouse/touch interaction through an html overlay** !

If you'd like to optimize some Math methods, you may use :

    jProcessingJS(this, {optmath:true});

It will upgrade **round()**, **floor()**, **abs()** and **min()** methods with bitwise operations (brought from [jspeed](http://code.google.com/p/jspeed/)).

### Where ?

Just put one line of code **in your sketch's setup() section** !  
The use of jProcessingJS() will do what size() used to do (but better), so you'll have to remove size() from your sketch.  
Or at least call jProcessingJS() after you used size(), it'll override it.

### Who ?

I'm [Gildas P.](http://www.gildasp.fr), a french webdesigner.  
I've spent some time playing with ProcessingJS, and found it great... and greater after [some JS tinkering](http://playingwithpixels.gildasp.fr) !

### Live examples ?

Coming soon on my blog : [http://playingwithpixels.gildap.fr](http://playingwithpixels.gildap.fr).  
You may already download the examples here, in the example folder, or download the zip file.

### More ?

There's more to come.  
I'm currently working on **advanced image preloading**, in order to be able to play some basic sketch while loading, and the real stuff once it's done.  
Another usefull thing would be to start the sketch only when the audio files are loaded too, for example... or any other assets you'd need in your sketch.  
Obviously I'll have to deal with webfonts the same way, which is far more complicated.  
Wait'n see !

---

#### LICENSE

MIT