## things-fullscreen-behavior

en-us

A simple Polymer `behavior` that wraps the HTML5 full screen API.
It lets you define which element to display in full screen mode
(via the `target` attribute) and toggle normal/full screen
mode by calling the `toggleFullscreen()` method.
Note that this method MUST be triggered directly by user interaction
(typically in a native `onclick` or Polymer's `on-click` handler).
If no `target` is set, the whole page (more specifically
`document.documentElement`) will be displayed full screen.
The element also provides 2 read-only flags as attribute:
- `fullscreenAvailable`: set to `true` if the browser supports
   HTML5's full screen API (Safari on iOS does not).
- `fullscreen`: set to `true` if an element is currently displayed in
   full screen mode.

##

ko-kr

HTML5 full screen API를 래핑하는 간단한 Polymer 'behavior'
전체 화면 모드로 표시 할 element를 정의 할 수 있고(target속성으로 통함),
'toggleFullscreen()'method를 호출함으로써 normal/full화면모드로 전환할 수 있다.
이 방법은 반드시 사용자 상호 작용에 의해 직접 트리거 되어야 한다.
(일반적으로 원래의 'onclick' 또는 Polymer의 'on-click'핸들러)
만일 'targer'이 set되어 있지 않으면, 전체 page가 fullscreen으로 display될 것이다.
이 element는 또한 속성으로부터 read-only flag들이 제공된다.
- 'fullscreenAvailable' : HTML5의 전체 화면 API를 브라우저가 지원하는 경우 'true'로 설정(iOS Safari에서는 안됨)
- 'fullscreen' : 현재 full screen mode로 되어있다면 'true'로 설정.


## Dependencies

Element dependencies are managed via [Bower](http://bower.io/). You can
install that via:

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
`http://localhost:8080/components/things-date-picker/`, where `things-date-picker` is the name of the directory containing it.


## Example 1. Things fullscreen
`<things-fullscreen>` Things fullscreen
