# Подготовка Windows

1. В Windows переходим в `Control Panel (Панель управления)` =&gt; `Programs and Features (Программы и компоненты)` =&gt; `Turn Windows features on or off (Включение или отключение компонентов в Windows)`  
   ![](/Development/TestSystem/PrepairingWindows/1.jpg)

2. Выделяем все компоненты входящие в Internet Information Services за исключением WebDAV Publishing \(Веб-публикация DAV\) и жмем OK  
   ![](/Development/TestSystem/PrepairingWindows/2.jpg)

3. Переходим в `C:\Program Files\WebSoft`, жмем по папке `WebTutorServer` правой кнопкой мыши, затем на `Properties (Свойства)`  
   ![](/Development/TestSystem/PrepairingWindows/3.jpg)

4. В закладке `Security (Безопасность)`, жмем `Edit... (Изменить...)`

   ![](/Development/TestSystem/PrepairingWindows/4.jpg)

5. В открывшемся окне выбираем группу `Пользователи` и ставим галку `Full Control`

   ![](/Development/TestSystem/PrepairingWindows/5.jpg)

6. Затем жмем `Add... (Добавить)`, в открывшемся окне пишем `Network Service`, жмем `Check Names (Проверить имена)`, затем `OK`  
   ![](/Development/TestSystem/PrepairingWindows/6.jpg)

7. Выбираем появившуюся группу `NETWORK SERVICE` и ставим галку напротив `Full Control`, после чего жмем `OK`

   ![](/Development/TestSystem/PrepairingWindows/7.jpg)

8. Аналогично нужно выдать права группе `Пользователи` для папки `C:\Program Files\WebSoft\WebTutorAdmin`

9. **Внимание!           
   **На данном этапе будьте особенно внимательны и делайте точно, как здесь написано, иначе велика вероятность, что на следующих этапах установки возникнут ошибки.  
   У многих людей из-за некорректного исполнения данного этапа на последующих этапах, возникали различные "эксклюзивные" ошибки, на решение которых уходило по несколько дней, хотя проблема скрывалась именно тут.

   Запускаем 64-битную командную строку от имени администратора `C:\Windows\SysWOW64\cmd.exe`  
   Запускаем 32-битную командную строку от имени администратора `C:\Windows\System32\cmd.exe`

   Командные строки запускаем как показано на принтскрине:  
   ![](/Development/TestSystem/PrepairingWindows/8.jpg)

   В 32-битной командной строке пишем:  
   `cd C:\Program Files\WebSoft\WebTutorServer\storage` + Enter  
   `install64.cmd` + Enter  
   В 64-битной командной строке:  
   `cd C:\Program Files\WebSoft\WebTutorServer\storage` + Enter  
   `install32.cmd` + Enter



