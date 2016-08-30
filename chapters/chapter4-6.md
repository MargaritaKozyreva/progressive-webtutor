# Костыли & Велосипеды

| Ссылка | Описание
| -- | -- |
| [#](#1) | Добавить настраиваемый Web шаблон (из раздела "Шаблоны документов") на страницу. |
| [#](#2) | Добавить скрипт из файла. |


<a name="#1"></a>
**Добавить на страницу настраиваемый Web шаблон (из раздела "Шаблоны документов")**
```html
<link rel="stylesheet" type="text/css" href="custom_web_template.html?object_id=<%=ArrayFirstElem(XQuery("for $elem in custom_web_templates where $elem/code=5796971352983414117 return $elem")).id%>"/>
```

<a name="#1"></a>
**Добавить скрипт из файла.**
```js
// Добавляем скрипт из файла
var Super = OpenCodeLib("x-local://wt/web/super-scripts/super.js");

// Используем функцию из подгруженного файла
var text = 'Privet'
Super.Hello(text);
```