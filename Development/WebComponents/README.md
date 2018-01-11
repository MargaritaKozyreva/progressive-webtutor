# Web components

Сразу надо понять, веб-компоненты - это не какая-то очередная библиотека, это часть платформы\(браузера\), которая уже давно делается W3C\(~ c 2012 года\) и усиленно продвигается Google и используются во многих крупных компаниях в продакшн \(YouTube, Bloomberg, EA итд\). То есть как все это работает рано или поздно придется изучить, так как это уже настоящее и будущее web.

Чтобы иметь представление о чем речь, посмотрите [по ссылке](https://vaadin.com/elements/browse), что они из себя представляют.

Веб-компоненты могут быть простыми и представлять из себя [кнопку](https://www.webcomponents.org/element/PolymerElements/paper-button), а могут быть огромными, включать в себя много других компонент, которые будут включать в себя еще компоненты и в итоге представлять из себя полноценные [приложения](https://santatracker.google.com).

#### Спецификации

В основе веб-компонент лежит четыре спецификации \(каждая может быть использована отдельно\):

1\) [Custom Elements](https://w3c.github.io/webcomponents/spec/custom/)

Создание собственных HTML-элементов

2\) [Shadow DOM](https://w3c.github.io/webcomponents/spec/shadow/)

Инкапсуляции DOM и CSS

3\) [&lt;script type="module"&gt;](https://jakearchibald.com/2017/es-modules-in-browsers/)

Загрузка веб-компонент

**Внимание! **Раньше для этого использовался [HTML imports](https://w3c.github.io/webcomponents/spec/imports/)\(`<link rel="import">`\). Но в 2017 было решено использовать ES6 Modules. Вы будете частенько встречать метод загрузки через HTML imports, его работу будут поддерживать еще несколько лет.

4\) [HTML Template](https://html.spec.whatwg.org/multipage/scripting.html#the-template-element/)

Отложенный рендер клиентского контента, который не отображается во время загрузки, но может быть инициализирован при помощи JavaScript.

---

Помимо спецификации, почитайте еще вот [тут](https://developers.google.com/web/fundamentals/web-components/).

#### 

#### Поддержка браузерами

Веб-компоненты можно использовать в браузерах, в которых реализованы 4 указанные выше спецификации.

На данный момент все четыре спецификации реализована в Chrome, Safari и Opera. В остальных браузерах они реализованы частично.

Пока остальные браузеры занимаются у себя осуществлением поддержки недостающих спецификаций\(а им это придется сделать\), для них был разработан полифилл [webcomponentsjs](https://github.com/webcomponents/webcomponentsjs), который добавляет поддержку спецификации в браузерах, в которых она отсутствует. Если вкратце, то полифилл [webcomponentsjs](https://github.com/webcomponents/webcomponentsjs), это просто скрипт, который добавляется на страницу и в зависимости от браузера, осуществляет поддержку отсутствующих спецификаций.

На данный момент поддержка веб-компонент браузерами выглядит вот так:

![](/Development/WebComponents/1.jpg)**Поддержка Internet Explorer**

Смею предположить, что вы\(как и большинство\) являетесь страстным "поклонником" браузера IE и хотите знать, как обстоят дела с поддержкой веб-компонент в IE? Кто бы мог подумать, но IE11 и его предки не поддерживают ни одной указанной выше спецификации...

В IE11 выручает полифилл [webcomponentsjs](https://github.com/webcomponents/webcomponentsjs) и добавляет поддержку всех четырех спецификаций и тогда веб-компоненты в нем работают.

Что касается предыдущих версий IE, то я наткнулся и на поддержку веб-компонент в IE9, IE10 в [X-Tag](https://x-tag.github.io/) \(библиотека для создания веб-компонент от Microsoft\). Но фишка в том, что X-Tag, как и все остальные, кто сейчас имеет дело с веб-компонентами используют один и тот же полифилл [webcomponentsjs](https://github.com/webcomponents/webcomponentsjs). И вот, что сказано по поводу поддержки в старых браузерах на странице полифилла [webcomponentsjs](https://github.com/webcomponents/webcomponentsjs):

_Полифилл может работать и в старых браузерах, однако для его использования потребуются дополнительные полифиллы \(такие как classList или другие полифиллы _[_платформы_](https://github.com/webcomponents/webcomponents-platform)_\). Мы не можем гарантировать поддержку для браузеров вне нашей матрицы совместимости._

В матрице совместимости у них указан только IE11+.

Microsoft перестал поддерживать все версии IE кроме IE 11 еще в 2016 году.

Проверять работу веб-компонент сделанных с помощью X-Tag в старых браузерах, нет ни времени ни желания\(так как даже IE11 поддерживать не хочется, не говоря про IE9, IE10\). "Хочется" конечно верить, что поддержка IE9, IE10 действительно есть. Но пока этого никто не проверил рассчитывайте на поддержку только IE11.

P.S. Если кто проверит поддержку веб-компонент сделанных с помощью X-Tag\(или с помощью чего-то еще\) в IE9, IE10 и она действительно есть, отпишите мне я обновлю информацию.



## Conclusion {#conclusion}

For the first time ever, we have an API primitive that does proper CSS scoping, DOM scoping, and has true composition. Combined with other web component APIs like custom elements, shadow DOM provides a way to author truly encapsulated components without hacks or using older baggage like`<iframe>`s.

Don't get me wrong. Shadow DOM is certainly a complex beast! But it's a beast worth learning. Spend some time with it. Learn it and ask questions!

