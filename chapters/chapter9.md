# Советы

Советы, которые помогут не наступить на грабли.

* Не изменяйте системные файлы и шаблоны WebTutor. Вносите свои изменения в систему путем добавления своих файлов и шаблонов.

---

WebTutor приходится переодически обновлять и патчить. Когда вы изменяете системные файлы, то при обновлении все ваши изменения теряются. С шаблон

* Do not change the basic system files and templates Webtutor. Try modifying the system by adding your files. Copy the existing elements of the system and make changes in the copy of elements.

* If possible, try not use server-side Javascript. Try use Webtutor as the database server, get data in JSON/XML format and calmly work with received information on the client side.

* When you make a POST request to the WebTutor server, use standard JavaScript object in the body of the request. (content-type="application/x-www-form-urlencoded")

* Responses from the Webtutor server do in JSON or XML format.

**Example:**

```js
<%
//Create object
obj = {};

//Fill object
obj.param = true;
obj.array = XQuery("for $elem in groups return $elem");

//Convert to JSON or XML
json_string = tools.array_to_text(obj, 'json');
%>

//Display server response
<%=json_string%>
```