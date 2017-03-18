# EvalCodeUrl\(\)

```js
/**
 * Загружает код на JavaScript из заданного url и выполняет его.
 * @param {String} codeUrl url, содержащий код
 * @param {String} subCode вспомогательный код, выполняемый после выполнения основного кода. Как правило, содержит вызов функции, описанный в основном коде. Необязательный аргумент. 
 * @return {Any}
 */
function EvalCodeUrl(url, subCode) {...}

// Пример
EvalCodeUrl('backup/rcr_lib_backup.js', 'RunBackup()')
```

**Внимание!**

Использование данной функции для вызова функций, описанных в файле, не рекомендуется после появления функции [OpenCodeLib\(\)](/Code/Functions/CodeExecution/OpenCodeLib.md), предлагающей более понятные правила области видимости переменных:

```js
OpenCodeLib( 'rcr_lib_backup.js' ).RunBackup()
```



