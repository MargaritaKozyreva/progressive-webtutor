# EncodeCharset\(\)

```js
/**
 * Переводит строку из кодировки, используемой  в программе по умолчанию, в заданную кодировку. На текущий момент поддерживаются кодировки windows-1251, windows-1252, utf-8, utf-16, koi8-r, cp-866
 * @param {String} str строка
 * @param {String} str имя кодировки, в которую нужно перевести строку
 * @return {Integer}
 */
function EncodeCharset(str, charset) {...}

// Пример
EncodeCharset(sampleString,'utf-8');
```



