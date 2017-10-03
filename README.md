# w3wtify.js library ![](http://www.geotekne.com.ar/w3wtify/img/w3wtify.png)

This Javascript library allows you to embed and use [What3Words](https://www.what3words.com) in your site easily.

**What is What3Words ?**

what3words is the simplest way to talk about any precise location. The system divide the world into a grid of 3m x 3m squares and assign each one a unique address made of just 3 words. In that way everyone and everywhere has a reliable address.

For a longer description, we suggest to watch this [![video w3w](https://img.youtube.com/vi/JTy7C47I8w0/0.jpg)](https://www.youtube.com/watch?v=JTy7C47I8w0)

* * *

## Features & Interface

Using w3wtifyJS you can easily integrate What3Words addressing system in your website.

Main features are:

*   Embed a GoogleMap with a icon for searching a W3W address code, in any DIV element you decide, and as many times as you need.
*   Inject JS code that allows you -based on a selected event- to open a W3W Modal widget.

Look at the examples below to understand how to use those features.
Additionally, you can customize the widget based on this interface:

### Tokens

It's mandatory to set them with your own values for your webpage, otherwise library won't work.

*   'w3w_token':  
    What3words token required in order to use W3W API. Check [What3Words Developers Section](https://what3words.com/developers/)

*   'w3w_gmaps_key':  
    Your GoogleMaps KEY that allows to show maps in widgets. Check [Google Maps API Key](https://developers.google.com/maps/documentation/javascript/get-api-key)

### W3W Modal Widget parameters

All parameters have some default value, providing a simple user experience when loading the library.

*   'w3w_modalEnabled':  
    Disables or enables the modal in a page. By default value is true.

*   'w3w_attachModalListener':  
    If modalEnabled is true, you can even decide if you want or not to allow attaching events to Modal listeners. By default value is true.

*   'w3w_showPreffixInModal':  
    Shows the W3W preffix in addresses or not. Preffix value is 'w3w.'. It allows to identify an address in a text (useful for various purposes). Default value is true.

*   'w3w_listenersSelector':  
    A selector list (CSS) of elements you would like to add as listeners in order to show the W3W modal. Example: 'input[type=text], input[type=search], textarea'

*   'w3w_listenersEvent':  
    Event id that will trigger the action of showing the W3W Modal. Example: 'click' or 'keyup'. In the case of 'keyup' the library will identify when the user writes the 'w3w preffix' for a search ('w3w.')

*   'w3w_listenersCallback':  
    Callback function that is triggered when the W3WModal is closed using the Insert button.

*   'w3w_initialMarkerPosition':  
    Initial position of search icon in the map. Latlon value by default is center of Tandil City.

*   'w3w_initialZoomLevel':  
    Initial zoom level for map in W3WModal. Default value: 4.

### Functions

With these 3 functions you can enable or disable the visual W3Wtify features in your webpage.

*   'insertW3WNodesInDiv':  
    Used to embed the W3W widget in a div.

*   'includeW3WModal':  
    When called, injects the W3WModal in your page.

*   'attachW3WListener':  
    When called, injects events listeners to selected elements defined in w3w_listenersSelector variable

### Other parameters/tools

*   'w3w_language':  
    Defines the language used when an address is asked to W3W Service. English by default ('en' value)

*   'w3w_debugging':  
    Allows to debug the w3wtify library. False value by default.

* * *

## Installation

In order to use W3Wtify in your website, you just need to insert a couple of javascript lines code at the bottom of your webpage, before closing the body tag, as shown in the example below.

It's only about 2 steps. First, to include the library, and second, to define your own API key values.

```
... // Include the library <script src="https://cdn.jsdelivr.net/gh/jemacchi/w3wtify@0.5/dist/w3wtify.min.js"></script>

// Define your keys and initialize widgets 
<script> 
    window.addEventListener('load', function() { 
         w3wtify.w3w_gmaps_key = '<yourGmapsKeyhere>'; // required
         w3wtify.w3w_token = '<yourW3WTokenhere>'; // required 
             
         // In this example, you include a W3W widget in the div called myW3WMap1 
         
         w3wtify.insertW3WNodesInDiv('myW3WMap1',false,{lat: 45.363, lng: 70.044}, 2); 
         
         // Calling includeW3WModal then you are injecting the W3WModal in your page
         // By default, library will open the Modal when you type 'w3w.' in an input[type=text]
         
         w3wtify.includeW3WModal(); },false); 
     
</script> 
</body> 
</html>
```

If you are a developer, check source code of this page and you will find some examples of use.

* * *

## Examples of Use

You can use the library to setup diverse W3W maps in your page. 
Please check  [W3Wtify project webpage](https://www.what3words.com) for examples.

* * *
## About W3Wtify

This library was developed by Jose Macchi (Geotekne) as part of a set of tools, plugins and addons that will use W3W technology in order to "facilitate people talking about a precise location".

Now working on:

*   W3Wtify Chrome plugin
*   W3Wtify Firefox addon
*   W3Wtify Safari addon
*   W3W Facebook Albums

* * *
Powered by [What3Words](https://www.what3words.com)

Developed by [Geotekne](http://www.geotekne.com.ar)