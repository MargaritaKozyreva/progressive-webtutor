# LoadFileData()

```js
/**
 * Загружает содержимое файла по заданному пути, результат возвращается в виде строки, содержащей бинарные данные.
 * @param {String} path путь к файлу
 * @return {String}
 */
function LoadFileData(path) {...}

// Пример
obj = LoadFileData(UrlToFilePath('x-local://wt/web/plugins/settings.json'));
// '{"settings": "..."}'
```