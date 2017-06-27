# things-fullscreen-behavior

## It is a behavior that supports full-screen mode of the screen.

A simple Polymer `behavior` that wraps the HTML5 full screen API.
It lets you define which element to display in full screen mode (via the `target` attribute) and toggle normal/full screen mode by calling the `toggleFullscreen()` method.

Note that this method MUST be triggered directly by user interaction
(typically in a native `onclick` or Polymer's `on-click` handler).

If no `target` is set, the whole page (more specifically `document.documentElement`) will be displayed in full screen.
The element also provides 2 read-only flags as attribute:
- `fullscreenAvailable`: set to `true` if the browser supports HTML5's full screen API (Safari on iOS does not).
- `fullscreen`: set to `true` if an element is currently displayed in full screen mode.

##

Example :

```html
<fullscreen-btn></fullscreen-btn>
<dom-module id="fullscreen-btn">
  <template>
    <style>
      :host {
        display: block;
      }
    </style>
    <button id="fullscreen-btn" on-tap="toggleFullscreen">fullscreen-btn</button>
  </template>
  <script>
    Polymer({
      is: 'fullscreen-btn',
      behaviors:[
        Things.FullscreenBehavior
      ]
    });
  </script>
</dom-module>
```

## Dependencies

Element dependencies are managed via [Bower](http://bower.io/). You can install that via:

    npm install -g bower

Then, go ahead and download the element's dependencies:

    bower install


## Playing With Your Element

If you wish to work on your element in isolation, we recommend that you use
[Polyserve](https://github.com/PolymerLabs/polyserve) to keep your element's
bower dependencies in line. You can install it via:

    npm install -g polymer-cli

And you can run it via:

    polymer serve

Once running, you can preview your element at
`http://localhost:8080/components/things-fullscreen/`, where `things-fullscreen` is the name of the directory containing it.
