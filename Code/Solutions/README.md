# Решения

| Ссылка | Описание |
| :--- | :--- |
| [\#](#добавить-настраиваемый-веб-шаблон-из-раздела-шаблоны-документов-на-страницу) | Добавить настраиваемый веб-шаблон из раздела "Шаблоны документов" на страницу. |
| [\#](#запрос-на-получение-списка-всех-настраиваемых-полей) | Запрос на получение списка всех настраиваемых полей. |
| [\#](#отправить-и-создать-клиентский-файл-на-сервере) | Отправить и создать клиентский файл на сервере. |

#### 

#### Добавить настраиваемый веб-шаблон из раздела "Шаблоны документов" на страницу.

```html
<link rel="stylesheet" type="text/css" href="custom_web_template.html?object_id=<%=ArrayFirstElem(XQuery("for $elem in custom_web_templates where $elem/code=5796971352983414117 return $elem")).id%>
```

#### 

#### Запрос на получение списка всех настраиваемых полей.

Если у вас SQL база, то данный объект хранится в таблице \[\(spxml\_blobs\)\].

Для получения списка полей сделайте запрос в SQL Server Managment Studio:

```sql
SELECT *, CONVERT(xml,(data )) as xml_data 
FROM [(spxml_blobs)]
WHERE url like '%custom_templates%'
```

#### 

#### Отправить и создать клиентский файл на сервере.

Создайте в корне вашего сайта файл \_save-file.html с наполнением ниже и откройте его

\(данный код будет сохранять файл любого формата в корне сайта\)

\(код тестовый, для общего понимания процесса, для использования на живой системе, надо продумать о безопасность\)

```js
<%
if(Request.UrlParam === 'save') {
var body = tools.read_object(Request.Body, 'json')
PutFileData(UrlToFilePath('x-local://wt/web/_' + body.name), Base64Decode(body.data))

var newDoc = tools.new_doc_by_name('resource')
root = newDoc.resource
root.name = body.name
root.file_name = body.name
root.file_url = 'x-local://wt/web/_' + body.name
newDoc.BindToDb(DefaultDb)
newDoc.Save()
}
%>
```

```html
<input type="file">
<button onclick="save()">Save</button>
```

```js
<script>
function save() {
    var file = document.querySelector('input').files[0]
    if (file) {
        var reader = new FileReader()
        reader.readAsDataURL(file)
        reader.onload = function(e) {
            var data = e.target.result.replace('data:' + file.type + ';base64,', '')
            xhr({
                "name": file.name,
                "data": data
            })
        }
    }
}

function xhr(body) {
    var xhr = new XMLHttpRequest()
    xhr.open("POST", "/_save-file.html?save")
    xhr.send(JSON.stringify(body))
    xhr.onreadystatechange = function() {
        if (xhr.readyState === 4 && xhr.status === 200) {
            alert("Saved")
        }
    }
}
</script>
```



