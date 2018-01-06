# ObtainDirectory\(\)

```js
/**
 * Проверяет, существует ли указанная директория, если нет - создает ее.
 * @param  {String} path путь до файла
 * @param  {Boolean} copyPath создавать всю цепочку родительских директорий, если они не существуют. Необязательный аргумент.
 * @return {undefined}
 */
function ObtainDirectory(path, isRecursive) {...}

// Пример
ObtainDirectory('x-local://wt/web/plugins/name/', true);
```



