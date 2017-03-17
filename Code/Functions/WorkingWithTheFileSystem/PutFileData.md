# PutFileData()
```js
/**
 * Сохраняет содержимое строки в файл. Содержимое строки интерпретируется как бинарные данные.
 * @param {String} path путь к файлу
 * @param {String} str данные
 * @return {undefined}
 */
function PutFileData(path, str) {...}

// Пример
// Создадим excel файл на сервере
excel_string = "<table border=1 cellpadding=5 cellspacing=0 style='border-collapse:collapse' width='100%'>";
excel_string += "<tr><td>ФИО</td><td>Должность</td></tr>";
excel_string += "<tr><td>Иванов Иван Иванович</td><td>Специалист</td></tr>";
excel_string += "</table>";

PutFileData(UrlToFilePath('x-local://wt/web/reports/excel_file.xls'), excel_string);
```
