# Запуск WebTutor

1. Заходим в IIS и запускаем: 


   **Сервер**
    ![](/Development/TestSystem/StartWebTutor/1.jpg)
   **Пул WebTutorCorpServer**
   ![](/Development/TestSystem/StartWebTutor/2.jpg) 

   **Сайт WebTutorCorpServer**
   ![](/Development/TestSystem/StartWebTutor/3.jpg)

2. Открываем в браузере страницу [https://localhost:8787](https://www.gitbook.com/book/maksimyurkov/progressive-webtutor/edit#), она будет в статусе загрузки.
   Загружаться она будет до тех пор, пока в SQL базе данных `wt` не создадутся все необходимые таблицы WebTutor, это займет ~ минут 10. \(можете посмотреть как таблицы появляются в SSMS\)
   ![](/Development/TestSystem/StartWebTutor/4.jpg)

3. Когда создание таблиц в SQL завершится, по адресу [https://localhost:8787](https://localhost:8787) будет такая картина
   ![](/Development/TestSystem/StartWebTutor/5.jpg) 
4. Запускаем WebTutor Administrator

5. Пишем `localhost:8787`  
   ![](/Development/TestSystem/StartWebTutor/6.jpg)

6. Нажимаем на `Русский`  
   ![](/Development/TestSystem/StartWebTutor/7.jpg)

7. Вводим логин: `user1`, пароль: `user1`, жмем `ОК`  
   ![](/Development/TestSystem/StartWebTutor/8.jpg)

8. Переходим в  `Портал` - `Узлы` - `Хост по умолчанию`  
   ![](/Development/TestSystem/StartWebTutor/9.jpg)

9. Меняем порт на `8787`  
   ![](/Development/TestSystem/StartWebTutor/10.jpg)

10. После этого портал начнет корректно открываться по адресу [https://localhost:8787](https://localhost:8787)  
    ![](/Development/TestSystem/StartWebTutor/11.jpg)



