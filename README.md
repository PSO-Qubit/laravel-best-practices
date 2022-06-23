# Хорошие практики Laravel

## Организация БД

1. В сложных таблицах ключом является суррогатный id
2. В простых справочниках ключом является естественный id
3. id на английском языке - добавляется колонка перевода на русском "name"
4. Нужно заранее определиться с принципами определения длины строк в БД


## Разграничение прав доступа

1. Вынос логики контроля доступа к страницам в middleware
2. Создание справочника ролей
3. Создание справочника видов разрешений (не проверял)
4. Создание таблицы "Роли-Разрешения"


## Эргономика кода

1. JavaDoc-комментарии для публичного API
2. private-методы внутри контроллеров выносятся в ServiceLayer
3. Логика предметной области выносится в ServiceLayer - контролер только вызывает нужный метод
4. Написание валидаторов-request происходит до написания основного кода


## CI/CD (пока условно)

1. Две ветки: main и feature
2. main - стабильные версии кода. Обновляется иногда
3. feature - обновляется ежедневно
