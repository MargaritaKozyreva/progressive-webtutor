# UrlToFilePath()

```js
/**
 * Преобразует локальный URI типа file: или x-local: в путь файловой системы.
 * @param  {String} URI локальный URI
 * @return {String}
 */
function UrlToFilePath(URI) {...}

// Пример
UrlToFilePath('x-local://wt/web/plugins/akismet/plugin-config.json');
// "C:\Program Files\WebSoft\WebTutorServer\wt\web\plugins\akismet\plugin-config.json"
```