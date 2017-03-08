# ArrayFind\(\)

```js
/**
 * Находит первый элемент массива, удовлетворяющий заданному условию. Если элемент, удовлетворяющий условию, не найден, функция завершается с исключением.
 * @param  {Array}  array     массив
 * @param  {String} qualExpr  выражение, определяющее соответствие элемента массива критерию. Вычисляется относительно элемента массива
 * @return {undefined}
 */
function ArrayFind(array, qualExpr) {...}

// Пример
ArrayFind(XQuery("for $elem in events return $elem"),'This.duration_fact>50');
```



