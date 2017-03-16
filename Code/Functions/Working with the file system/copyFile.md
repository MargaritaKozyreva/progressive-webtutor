# copyFile()

```js
/**
 * Копирует файл.
 * @param  {String} filePath путь до файла
 * @param  {String} copyPath путь до места копирования
 * @return {undefined}
 */
function copyFile(filePath, copyPath) {
  PutFileData(copyPath, LoadFileData(filepath));
}

// Пример
copyFile('x-local://wt/web/assets/file.txt', 'x-local://wt/web/assets/copy/copy.txt');
```