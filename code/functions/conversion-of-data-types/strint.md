# StrInt\(\)

```js
/**
 * Преобразует целочисленный аргумент в строку.
 * @param {Integer} arg           целое число
 * @param {Integer} digitsNum     минимальное число символов в строке. Недостающие символы компенсируются нулями перед числом. Необязательный аргумент.
 * @param {Boolean} addGroupDelim разделять тысячные разряды пробелами. Необязательный аргумент.
 * @return {String}
 */
function StrInt(arg, digitsNum, addGroupDelim) {...}

// Пример
StrInt(11500);
// '11500'

StrInt(11500, 6);
// '011500' 

StrInt(11500, 0, true);
// '11 500'
```



