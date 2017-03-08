# ArraySelect\(\)

```js
/**
 * Выбирает элементы массива, удовлетворяющие заданному критерию.
 * @param  {Array} array   массив
 * @param  {Boolean} qulExpr ID выражение, определяющее соответствие элемента массива критерию. Вычисляется относительно элемента массива.
 * @return {Array}
 */
function ArraySelect(array, qulExpr) {...}

// Пример
// Выбрать элементы у которых атрибут 'basic_collaborator_id' содержит значение
ArraySelect(XQuery("CatalogHierSubset('subs', 5296742292364664534)"), "basic_collaborator_id.HasValue");

// Выбрать элементы которые удовлетворяют условию
ArraySelect(XQuery("for $elem in learnings return $elem"),'This.score>10');
```



