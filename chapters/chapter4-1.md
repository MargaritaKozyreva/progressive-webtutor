# Синтаксис

Система Webtutor работает на платформе SP-XML, которая имеет встроенный интерпретатор JavaScript. 

Для исполения кода на стороне сервера его следует заключать в теги:

* `<%`...`%>`

```js
<%
// Добавит запись "Hello, World!" в лог сервера (\WebTutorServer\Logs\xhttp-YYYY-MM-DD.txt)
alert('Hello, World!');
%>
```
Для вывода строки используйте теги: 

* `<%=`...`%>` 

```html
<div>
<!-- Добавит строку "Hello, World!" in div element-->
  <%="Hello World!"%>
</div>
```

  Все, что находится за пределами тегов отображается без изменений. В основном это используется для формирования содержимого файлов (html, css, js, json итп): 
  
  **До обработки:**

```html
<%
title = "Page Title";
arr = ['one','two','three'];
%>
<html>
	<head>
	  <title><%=title%></title>
	</head>
	<body>
		<%
		for(i in arr) {
		%>
			<p><%=i%></p>
		<%
		}
		%>
	</body>
</html>
```

**После обработки:**

```html
<html>
	<head>
	  <title>Page Title</title>
	</head>
	<body>
		<p>one</p>
		<p>two</p>
		<p>three</p>
	</body>
</html>
```
В остальном синтаксис кода напоминает старые версии JavaScript.