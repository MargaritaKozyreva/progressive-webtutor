# StrRealFixed\(\)

```js
/**
 * Преобразует вещественный аргумент в строку, с фиксированным количеством символов в дробной части.
 * @param {Real} arg              вещественный аргумент
 * @param {Integer} pricision     число символов в дробной части числа. Недостающие символы компенсируются нулями. 
 * @param {Boolean} addGroupDelim разделять тысячные разряды пробелами. Необязательный аргумент.
 * @return {String}
 */
function StrRealFixed(arg, pricision, addGroupDelim) {...}

// Пример
StrRealFixed(90154.2);
// '90154.20'

StrRealFixed(90154.2, 2, true);
// '90 154.20'
```



