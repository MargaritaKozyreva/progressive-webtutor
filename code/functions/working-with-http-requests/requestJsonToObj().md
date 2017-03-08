# requestJsonToObj\(\)

```js
/**
 * Получает объект переданный в формате JSON методом POST.
 * @return {Object}
 */
function requestJsonToObj() {
  return tools.read_object(Request.Body, "json");
}

// Пример
var requestObj = requestJsonToObj();
```



