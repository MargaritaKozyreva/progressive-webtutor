# Проверяем инкапсуляцию

Проверим действительно ли все так, как написано в спецификации веб-компонент и их DOM c CSS инкапсулированы.

Для этого понадобится текстовый редактор и [Node.js](https://nodejs.org/en/).

В командной строке:

Установим сервер, который будем использовать во время разработки:

`npm install polyserve -g` + Enter

Создадим каталог в котором будем работать:

`cd C:\` + Enter

`mkdir check-incapsulation` + Enter

`cd check-incapsulation` + Enter

Запускаем сервер

`polyserve` + Enter

## Проверка в Chrome

Сначала проверим как работает инкапсуляция в браузере где реализована поддержка всех четырех спецификаций веб-компонент.

В каталоге `check-incapsulation` создадим файл index.html с таким содержимым

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <script type="module" src="/my-clock.js"></script>
    <style>
    h2 {
        text-decoration: underline;
    }
    </style>
</head>

<body>
    <h2>Привет! Я заголовок снаружи Shadow DOM!</h2>
    <my-clock></my-clock>
</body>

</html>
```

и my-clock.js с таким

```js
'use strict'
class MyClock extends HTMLElement {
    connectedCallback() {
        let template = document.createElement('template')
        template.innerHTML = `
        <style>
            h2 {
                color: maroon;
                border-left: 3px solid maroon;
                padding: 8px 16px;
                font-family:'Roboto';
                font-weight: 300;
            }
        </style>
        <h2>Привет! Я заголовок внутри Shadow DOM!</h2>
        `
        this.attachShadow({
            mode: 'open'
        })
        this.shadowRoot.appendChild(document.importNode(template.content, true))
    }
}

customElements.define('my-clock', MyClock)
```

Смотрим результат в Chrome![](/Development/CheckEncapsulation/1.jpg)Супер! Все работает как и задумано. CSS снаружи веб-компоненты не попадает в нее, а CSS внутри не выходит наружу.

## Проверка в IE11

А теперь попробуем тоже самое в браузере, который не поддерживает ни одной из четырех спецификаций веб-компонент.![](/Development/CheckEncapsulation/2.jpg)Ничего не работает. Попробуем подключить полифиллы, которые добавят поддержку необходимых спецификаций.

Все необходимые полифиллы находятся в модуле [webcomponentsjs](https://github.com/webcomponents/webcomponentsjs). Установим его.

В командной строке пишем 

`npm install @webcomponents/webcomponentsjs` + Enter

В index.html делаем вот так

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <script src="/node_modules/@webcomponents/webcomponentsjs/webcomponents-lite.js"></script>
    <script type="module" src="/my-clock.js"></script>
    <script nomodule src="/my-clock.js"></script>
    <style>
    h2 {
        text-decoration: underline;
    }
    </style>
</head>
<body>
    <h2>Привет! Я заголовок снаружи Shadow DOM!</h2>
    <my-clock></my-clock>
</body>
</html>

```

Что мы изменили:

* Добавили на страницу скрипт webcomponents-lite.js, который добавит все необходимые полифиллы. Все будет работать, но добавил я webcomponents-lite.js только в демонстрационных целях. В реальных проектах такого делать не стоит. У webcomponentsjs довольно много возможностей загрузки. Во первых надо загружать асинхронно и загружать, только те полифиллы, которые будут необходимы, а не все, как это сделано сейчас. Подробности, как это делается, почитать на странице полифилла [webcomponentsjs](https://github.com/webcomponents/webcomponentsjs).
* Добавили `<script nomodule src="/my-clock.js"></script>`. Так как IE11 не знает, что такое `type="module"`, он это загружать не будет. А вот скрипт с `nomodule` загрузит. Современные же браузеры с поддержкой импорта модулей будут делать наоборот. Подробности можете почитать [тут](https://jakearchibald.com/2017/es-modules-in-browsers#nomodule-for-backwards-compatibility).

В my-clock.js делаем вот так

```js
'use strict'
let template = document.createElement('template')
template.innerHTML = `
<style>
    h2 {
        color: maroon;
        border-left: 3px solid maroon;
        padding: 8px 16px;
        font-family:'Roboto';
        font-weight: 300;
    }
</style>
<h2>Привет! Я заголовок внутри Shadow DOM!</h2>
`
ShadyCSS.prepareTemplate(template, 'my-clock')
class MyClock extends HTMLElement {
    connectedCallback() {
        ShadyCSS.styleElement(this)
        this.attachShadow({
            mode: 'open'
        })
        this.shadowRoot.appendChild(document.importNode(template.content, true))
    }
}

customElements.define('my-clock', MyClock)
```

Что мы изменили:

* Добавили пару строчек кода, тем самым осуществили частичную поддержку ShadowDOM и частичную инкапсуляцию CSS с помощью полифиллов [ShadyDOM](https://github.com/webcomponents/shadydom) и [ShadyCSS](https://github.com/webcomponents/shadycss) \(данные полифиллы уже встроены в webcomponentsjs не надо их отдельно подгружать\)

Смотрим результат:

![](/Development/CheckEncapsulation/3.jpg)

