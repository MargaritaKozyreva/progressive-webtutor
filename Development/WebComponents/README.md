# Web components

Веб-компоненты состоят из нескольких отдельных технологий.

Я и сам с осторожно отношусь к чему-то новому, так как в свое время уделил много времени Flash и ActionScript 3, от которых все в итоге отказались :D Но тут совсем другая ситуация. Веб-компоненты это не какая-то очередная библиотека, это часть платформы\(браузера\), которая уже давно делается W3C и усиленно продвигается Google и уже запущена во многих крупных компаниях в продакшн \(YouTube, Bloomberg, EA итд\).

Веб-компоненты основаны на четырех основных спецификациях \(каждая может быть использована отдельно\):

[Custom Elements](https://w3c.github.io/webcomponents/spec/custom/)

Возможность создавать собственные HTML-элементы

[Shadow DOM](https://w3c.github.io/webcomponents/spec/shadow/)

Возможность инкапсуляции DOM и CSS

[ES6 Modules](https://jakearchibald.com/2017/es-modules-in-browsers/)

Возможность загружать веб-компоненты

**Внимание! **Раньше для этого использовался [HTML imports](https://w3c.github.io/webcomponents/spec/imports/). Но в 2017 было решено использовать ES6 Modules. Вы будете частенько встречать метод загрузки через HTML imports\(тег `<link rel="import">`\) его работу будут поддерживать еще несколько лет.







HTML imports

The [HTML imports specification](https://w3c.github.io/webcomponents/spec/imports/)defines the inclusion and reuse of HTML documents in other HTML documents.

HTML Template

The [HTML template element specification](https://html.spec.whatwg.org/multipage/scripting.html#the-template-element/)defines how to declare fragments of markup that go unused at page load, but can be instantiated later on at runtime.

Вы можете думать о Веб-компонентах

** как о переиспользуемых виджетах пользовательского интерфейса,**

которые создаются с помощью открытых веб-технологий. Они являются частью браузера и поэтому не нуждаются во внешних библиотеках, таких как jQuery или Dojo.

Веб-компоненты могут быть простыми и представлять из себя к примеру [кнопку](https://www.webcomponents.org/element/PolymerElements/paper-button), а могут быть огромными, включать в себя много других компонент, которые будут включать в себя еще компоненты и в итоге представлять из себя полноценные [приложения](https://santatracker.google.com).

Веб-компоненты это не очередная библиотека или новая технология, существование которой под вопросом. Веб-компоненты утверждены и уже являются частью платформы и уже успешно используются во многих компаниях.

W3C

W3C еще вносит изменения в спецификацию, но эти изменения уже не значительные и можно уже спокойно использовать

#### Поддержка браузерами

[https://x-tag.github.io/](https://x-tag.github.io/)

Internet Explorer 9+

