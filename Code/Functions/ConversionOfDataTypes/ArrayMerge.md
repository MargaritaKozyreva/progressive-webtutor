# ArrayMerge\(\)

```js
/**
 * Возвращает строку, полученную путем склеивания данных из элементов массива.
 * @param {Array} array ма\ссив
 * @param {String} elemExpr выражение, вычисляющее значение, используемое для склейки, относительно элемента массива
 * @param {String} delim строка-разделитель. Необязательный аргумент.
 * @return {String}
 */
function ArrayMerge(array, elemExpr, delim) {...}

// Пример
ArrayMerge(groupDoc.TopElem.collaborators, "This.person_fullname", ",");
// "Васильева Людмила Петровна,Жирова Антонина Васильевна,Иванов Иван Иванович" 
```



