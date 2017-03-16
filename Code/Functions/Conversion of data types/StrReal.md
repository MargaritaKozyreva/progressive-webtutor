# StrReal\(\)

```js
/**
 * Преобразует вещественный аргумент в строку.
 * @param {Real} arg              вещественный аргумент
 * @param {Integer} pricision     максимальное число знаков после запятой (Integer). По умолчанию 6. Необязательный аргумент. 
 * @param {Boolean} addGroupDelim разделять тысячные разряды пробелами (Bool). Необязательный аргумент.
 * @return {String}
 */
function StrReal(arg, pricision, addGroupDelim) {...}

// Пример
StrReal(90154.249);
// '90154.249'

StrReal(90154.249, 2);
//'90154.25'

StrReal(90154.249, 2, true);
//'90 154.25'
```



