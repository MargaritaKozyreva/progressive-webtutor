# Request {#requestquerystringgetoptproperty}

Встроенный объект Request доступен на сервере xHttp.exe при вызове кода веб-страницы. Обозначает соответствующий HTTP-запрос к странице.

Информацию по всем доступным атрибутам и методам объекта Request вы можете получить по [ссылке](http://docs.datex.ru/article.htm?id=5665465792879477229).

```js
// Добавить заголовок в ответ сервера
Request.AddRespHeader("Access-Control-Allow-Origin","*");
```

```js
// Получить параметры переданные методом GET
// http://webtutor.otpbank.ru/view_doc.html?mode=home&code=345345&position=boss
Request.QueryString.GetOptProperty("mode", "");
// 'home'

Request.QueryString.GetOptProperty("code", "");
// '345345'

Request.QueryString.GetOptProperty("position", "");
// 'boss'

// Указать значение по умолчанию если параметр отсутствуюет
Request.QueryString.GetOptProperty("fail", 123);
```

```js
// Получить свойство объекта переданного методом POST
Request.Form.GetOptProperty("position", "");
```

```js
// Получить TopElem пользователя сделавшего запрос
Request.Session.Env.GetOptProperty('curUser', null);
```



