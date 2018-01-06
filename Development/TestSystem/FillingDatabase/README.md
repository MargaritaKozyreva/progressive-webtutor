# Наполнение базы данных

Если вы подключаете к тестовой системе свою\(наполненную\) базу данных, то можете пропустить данный раздел.

Хорошо если у вас есть возможность подключить к тестовой системе реально существующую, наполненную базу данных, но как быть если ее нет.

При установке WebTutor предоставляется возможность установить демонстрационные данные, но их там довольно мало и чтобы не вводить в дальнейшем путаницу мы при установке их не добавляли.

Можно вручную создавать карточки в WebTutor Administrator, но это очень долго и не так просто на лету что-то  придумывать и заполнять поля.

В данном разделе я покажу пару примеров, как можно наполнять базу данных. Наполним базу пользователями и курсами.

Потребуется [Node.js](https://nodejs.org/en/), установите, если его у вас нет.

## Создание сотрудников

Придумывать и создавать сотрудников вручную дело "такое". В интернете есть различные сервисы, которые генерируют данные пользователей в любых количествах. Мы будем использовать сервис [http://randomuser.ru](http://randomuser.ru).

Этапы создания:

1\) Генерируем json c данными 1000 пользователей. Проходим по ссылке [http://randomuser.ru/api.json?results=1000](http://randomuser.ru/api.json?results=1000) \(цифра в конце ссылки означает количество пользователей, выбирайте на свое усмотрение\) и сохраняем содержимое страницы в файл `C:\filler\users\users.json`.

2\) Создайте файл `C:\filler\users\get-avatars.js`  с таким содержимым:

```js
'use strict'
const request = require('request')
const fs = require('fs')

fs.readFile('users.json', (err, userData) => {
    console.log('Start')
    if (!fs.existsSync('avatars')) fs.mkdir('avatars')
    let data = JSON.parse(userData)
    let requestsArr = []
    let large, medium, thumbnail
    for (let i of data) {
        if (i.user.gender == "male") {
            large = i.user.picture.large.replace("http://randomuser.ru/images/men/", "")
            large = large.replace(".jpg", "-large-m.jpg")

            medium = i.user.picture.medium.replace("http://randomuser.ru/images/men/med/", "")
            medium = medium.replace(".jpg", "-medium-m.jpg")

            thumbnail = i.user.picture.thumbnail.replace("http://randomuser.ru/images/men/thumb/", "")
            thumbnail = thumbnail.replace(".jpg", "-thumbnail-m.jpg")
        } else {
            large = i.user.picture.large.replace("http://randomuser.ru/images/women/", "")
            large = large.replace(".jpg", "-large-w.jpg")

            medium = i.user.picture.medium.replace("http://randomuser.ru/images/women/med/", "")
            medium = medium.replace(".jpg", "-medium-w.jpg")

            thumbnail = i.user.picture.thumbnail.replace("http://randomuser.ru/images/women/thumb/", "")
            thumbnail = thumbnail.replace(".jpg", "-thumbnail-w.jpg")
        }

        requestsArr.push({
            "url": i.user.picture.large,
            "filename": large
        })
        requestsArr.push({
            "url": i.user.picture.medium,
            "filename": medium
        })
        requestsArr.push({
            "url": i.user.picture.thumbnail,
            "filename": thumbnail
        })
    }
    var j = 0
    var interval = setInterval(_ => {
        if (!(requestsArr.length < j)) {
            j++
            request(requestsArr[j].url, {
                encoding: 'binary'
            }, (error, response, body) => {
                fs.writeFile('avatars/' + requestsArr[j].filename, body, 'binary', _ => {})
                console.log(+(j / (requestsArr.length / 100)).toFixed(2) +'%')
            })
        } else {
            clearInterval(interval)
            console.log('100% Complete')
        }
    }, 3000)
})

```

3\) В командной строке вводим команды и ждем завершения скачивания изображений \(пока не будет написано 100% Complete\), займет это ~ 2.5 часа:  
  
cd C:\filler\users + Enter  
npm install fs + Enter  
npm install request + Enter  
node get-avatars.js + Enter  
  
4\) Копируем файл `C:\filler\users\users.json` и папку `C:\filler\users\avatars`

в 

