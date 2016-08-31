# Request.Form.GetOptProperty()

```js
/**
 * Получает значение свойства объекта переданного методом POST. Если запрос не содержит объект, атрибут возвращает ошибку.
 * @param {String} param   название параметра
 * @param {Any} default значение по умолчанию, возращаемое в случае отстутвия свойства. По умолчанию равен undefined. Необязательный аргумент.
 * @return {Any, Error}
 */
Request.Form.GetOptProperty(param, default);

// Пример
// Получаем свойства переданного объекта: {mode:'home',code:345345,position:'boss'}
Request.Form.GetOptProperty("mode", "");
// 'home'

Request.Form.GetOptProperty("code", "");
// '345345'

Request.Form.GetOptProperty("position", "");
// 'boss'
```