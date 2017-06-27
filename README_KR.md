# things-fullscreen-behavior

## 이는 전체 화면 모드를 지원하는 behavior이다.

이는 HTML5 전체 화면 API를 래핑하는 간단한 Polymer `behavior`이다.
(`target` 속성을 통해) 전체 화면 모드로 표시할 element를 정의하고, `toggleFullscreen()` 메소드를 호출하여 일반/전체 화면 모드를 토글할 수 있다.

이 방법은 반드시 사용자적 인터랙션(일반적으로 네이티브 `onclick` 또는 polymer의 `on-click` 핸들러)에 의해 직접 트리거되어야 한다는 점을 유의하여야 한다.

`target`을 설정하지 않으면, 전체 페이지(특히 `document.documentElement`)가 전체 화면으로 표시된다.
또한 이 element는 2 개의 읽기 전용 플래그를 속성으로 제공한다.
- `fullscreenAvailable`: 브라우저가 HTML5의 전체 화면 API를 지원하는 경우 `true`로 설정된다. (iOS의 Safari는 지원하지 않는다).
- `fullscreen`: 현재 전체 화면 모드로 표시되는 element가 있는 경우 `true`로 설정된다.

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

element의 종속성은 [Bower](http://bower.io/)를 통해 관리되며, 아래의 방법을 통해 설치할 수 있다.

    npm install -g bower

다음, element의 종속성을 다운로드한다.

    bower install


## Playing With Your Element

element를 독립적으로 처리하려면 [Polyserve](https://github.com/PolymerLabs/polyserve)를 사용하여 element의 bower 의존성을 유지하도록 하며, 이는 아래의 방법을 통해 설치할 수 있다.

    npm install -g polymer-cli

그리고, 아래의 방법을 통해 실행할 수 있다.

    polymer serve

element를 실행한 경우, `things-fullscreen`이 디렉토리 이름으로 포함되어 있는 `http://localhost:8080/components/things-fullscreen/`을 통해 이를 미리 확인할 수 있다. 
