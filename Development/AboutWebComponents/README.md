# О веб-компонентах

**Веб-компоненты** — технология, которая позволяет создавать многократно используемые компоненты в веб-документах и веб-приложениях. Веб-компоненты поддерживаются веб-браузерами напрямую и не требуют дополнительных библиотек для работы.

Модель веб-компонентов подразумевает[инкапсуляцию](https://ru.wikipedia.org/wiki/%D0%98%D0%BD%D0%BA%D0%B0%D0%BF%D1%81%D1%83%D0%BB%D1%8F%D1%86%D0%B8%D1%8F_%28%D0%BF%D1%80%D0%BE%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5%29)и[совместимость](https://ru.wikipedia.org/wiki/%D0%98%D0%BD%D1%82%D0%B5%D1%80%D0%BE%D0%BF%D0%B5%D1%80%D0%B0%D0%B1%D0%B5%D0%BB%D1%8C%D0%BD%D0%BE%D1%81%D1%82%D1%8C)отдельных[HTML-элементов](https://ru.wikipedia.org/wiki/%D0%AD%D0%BB%D0%B5%D0%BC%D0%B5%D0%BD%D1%82%D1%8B_HTML).

На данный момент частичная поддержка существует в[браузерах](https://ru.wikipedia.org/wiki/%D0%91%D1%80%D0%B0%D1%83%D0%B7%D0%B5%D1%80)[Chrome](https://ru.wikipedia.org/wiki/Google_Chrome),[Firefox](https://ru.wikipedia.org/wiki/Firefox),[Opera](https://ru.wikipedia.org/wiki/Opera)и[Safari](https://ru.wikipedia.org/wiki/Safari). Для браузеров не поддерживающих веб-компоненты реализованы[полифилы](https://ru.wikipedia.org/wiki/%D0%9F%D0%BE%D0%BB%D0%B8%D1%84%D0%B8%D0%BB).

Веб-компоненты включают четыре технологии, каждая из которых может использоваться отдельно от других:

* Custom Elements —
  [API](https://ru.wikipedia.org/wiki/API)
  для создания собственных
  [HTML](https://ru.wikipedia.org/wiki/HTML)
  элементов.
* HTML Templates — тег 
  &lt;
  template
  &gt;
   позволяет реализовывать изолированные
  [DOM](https://ru.wikipedia.org/wiki/Document_Object_Model)
  -элементы.
* Shadow DOM — изолирует DOM и стили в разных элементах.
* HTML Imports — импорт
  [HTML](https://ru.wikipedia.org/wiki/HTML)
  документов.

Стандартизацией данных технологий занимается[Консорциум Всемирной паутины](https://ru.wikipedia.org/wiki/%D0%9A%D0%BE%D0%BD%D1%81%D0%BE%D1%80%D1%86%D0%B8%D1%83%D0%BC_%D0%92%D1%81%D0%B5%D0%BC%D0%B8%D1%80%D0%BD%D0%BE%D0%B9_%D0%BF%D0%B0%D1%83%D1%82%D0%B8%D0%BD%D1%8B)\(W3C\). Текущие версии спецификаций располагаются в[GitHub](https://ru.wikipedia.org/wiki/GitHub)репозитории[webcomponents](https://w3c.github.io/webcomponents/).

