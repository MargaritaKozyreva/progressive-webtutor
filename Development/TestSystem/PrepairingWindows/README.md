# Подготовка Windows

1. В Windows переходим в Control Panel \(Панель управления\) =&gt; Programs and Features \(Программы и компоненты\) =&gt; Turn Windows features on or off \(Включение или отключение компонентов в Windows\)  
   ![](/Development/TestSystem/PrepairingWindows/1.jpg)

2. Выделяем все компоненты входящие в Internet Information Services за исключением WebDAV Publishing \(Веб-публикация DAV\) и жмем OK  
   ![](/Development/TestSystem/PrepairingWindows/2.jpg)

3. Переходим в C:\Program Files\WebSoft, жмем по папке WebTutorServer правой кнопкой мыши, затем на Properties \(Свойства\)  
   ![](/Development/TestSystem/PrepairingWindows/3.jpg)

4. В закладке Security \(Безопасность\), жмем Edit... \(Изменить...\)

   ![](/Development/TestSystem/PrepairingWindows/4.jpg)

5. В открывшемся окне выбираем группу Пользователи и ставим галку Full Control

   ![](/Development/TestSystem/PrepairingWindows/5.jpg)

6. Затем жмем Add..., в открывшемся окне пишем Network Service, жмем Check Names, затем OK  
   ![](/Development/TestSystem/PrepairingWindows/6.jpg)

7. Выбираем появившуюся группу NETWORK SERVICE и ставим галку Full Control, после чего жмем OK

   ![](/Development/TestSystem/PrepairingWindows/7.jpg)

8. Запускаем cmd.exe от имени администратора \(C:\Windows\SysWOW64\cmd.exe\) \(если у вас 32-битная система, тогда запустите C:\Windows\System32\cmd.exe\)  
   ![](/Development/TestSystem/PrepairingWindows/8.jpg)

9. Введите cd C:\Program Files\WebSoft\WebTutorServer\storage и нажмите Enter

10. Введите install32.cmd, нажмите Enter,

11. Если у вас 64-битный Windows, введите install64.cmd, нажмите Enter



