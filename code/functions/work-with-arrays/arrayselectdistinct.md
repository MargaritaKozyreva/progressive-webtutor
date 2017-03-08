# ArraySelectDistinct\(\)

```js
/**
 * Возвращает массив уникальных значений элементов заданного массива.
 * @param  {Array} array      массив
 * @param  {String} fieldExpr выражение, вычисляемое относительно каждого элемента исходного массива. Если аргумент не указан, используется значение самого элемента (This). Необязательный аргумент.
 * @return {Array}
 */
function ArraySelectDistinct(array, fieldExpr) {...}

// Пример
// Получить массив с уникальными значениями course_id
ArraySelectDistinct(XQuery('for $elem in learnings where $elem/person_id=5968567069372079247 return $elem'), 'course_id');
```



