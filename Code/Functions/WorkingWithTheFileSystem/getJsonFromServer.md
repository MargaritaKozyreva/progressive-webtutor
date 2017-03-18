# getJsonFromServer\(\)

```js
/**
 * Получает содержимое json файл и преобразовывает его в объект.
 * @param  {String} url путь до файла 
 * @return {Object}
 */
function getJsonFromServer(url) {
  return tools.read_object(LoadFileData(UrlToFilePath("x-local://wt/web/"+url)), "json");
}
```

**Внимание**

Если возникают проблемы при преобразовании, появляются лишние символы\(кавычки, разрывы строк итд\), то попробуйте сохранить json файл "Without BOM".

![](/Code/Functions/WorkingWithTheFileSystem/getJsonFromServer.jpg)

