# ReadDirectory()

```js
/**
 * Возвращает массив, содержащий список файлов и вложенных директорий внутри указанной директории. Каждый элемент массива будет содержать url вложенного файла или директории.
 * @param  {String} dirUrl путь до файла
 * @return {Array}
 */
function ReadDirectory(dirUrl) {...}

// Пример
ReadDirectory('x-local://wt/web/assets/');
/**
["value":"x-local://wt/web/plugins/course/bower.json",
"value":"x-local://wt/web/plugins/course/bower_components",
"value":"x-local://wt/web/plugins/course/data"]
*/
```