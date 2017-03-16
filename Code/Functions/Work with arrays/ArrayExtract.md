# ArrayExtract\(\)

```js
/**
 * Выбирает определенное значение из каждого элемента массива. Возвращает новый массив той же длинны, содержащий выбранные элементы.
 * @param  {Array} array      массив
 * @param  {String} fieldExpr выражение, вычисляемое относительно каждого элемента исходного массива
 * @return {Array}
 */
function ArrayExtract(array, fieldExpr) {...}

// Пример
// Взять из массива объектов только значения `id`
ArrayExtract(XQuery('for $elem in polls where $elem/is_main = true() return $elem'), 'id');
// [{id:5796971352983414117},{id:5296742292364664534},{id:5607317807203771898}]
```



