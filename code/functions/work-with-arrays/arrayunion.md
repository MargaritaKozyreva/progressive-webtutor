# ArrayUnion

```js
/**
 * Последовательное объединение нескольких массивов в один.
 * @param  {Array} array1 массив
 * @param  {Array} array2 массив
 * @return {Array}
 */
function ArrayUnion(array1, array2) {...}

// Пример
arr1 = XQuery("for $elem in test_learnings order by $elem/last_usage_date descending return $elem");
arr2 = XQuery("for $elem in active_test_learnings order by $elem/last_usage_date descending return $elem");
arr3 = XQuery("for $elem in active_learnings order by $elem/last_usage_date descending return $elem");
arr4 = XQuery("for $elem in learnings order by $elem/last_usage_date descending return $elem");
all = ArrayUnion(arr1, arr2, arr3, arr4);
```



