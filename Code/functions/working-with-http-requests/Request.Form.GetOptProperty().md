# Request.QueryString.GetOptProperty\(\) {#requestquerystringgetoptproperty}

```js
/**
 * Получает значение параметра URL переданного методом GET.
 * @param {String} param   название параметра
 * @param {Any} default значение по умолчанию, возращаемое в случае отстутвия параметра. По умолчанию равен undefined. Необязательный аргумент.
 * @return {Any}
 */
Request.QueryString.GetOptProperty(param, default);

// Пример
// Получим параметры из URL: http://webtutor.otpbank.ru/view_doc.html?mode=home&code=345345&position=boss
Request.QueryString.GetOptProperty("mode", "");
// 'home'

Request.QueryString.GetOptProperty("code", "");
// '345345'

Request.QueryString.GetOptProperty("position", "");
// 'boss'

Request.QueryString.GetOptProperty("fail", 123);
// 123
```



