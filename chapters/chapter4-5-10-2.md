# Request.Form.GetOptProperty()

```js
/**
 * Получает значение параметра URL переданного методом GET.
 * @param {String} param   название параметра
 * @param {Any} default значение по умолчанию, возращаемое в случае отстутвия параметра. По умолчанию равен undefined. Необязательный аргумент.
 * @return {Any}
 */
Request.QueryString.GetOptProperty(param, default);

// Пример
//Get paramemeters from Object: {mode:'home',code:345345,position:'boss'}
mode = Request.Form.GetOptProperty("mode", "");
//mode = 'home'
code = Request.Form.GetOptProperty("code", "");
//code = '345345'
position = Request.Form.GetOptProperty("position", "");
//position = 'boss'
```