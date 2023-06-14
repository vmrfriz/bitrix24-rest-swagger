# bitrix24-rest-swagger
Присоединяйтесь к совершенствованию. 

## Обновления
`14.06.2023` - Опубликован веб-интерфейс Swagger на Github Pages.

`27.05.2023` - Сделан набросок swagger-файла из [раздела документации "Общие методы"](https://dev.1c-bitrix.ru/rest_help/general/index.php).

## Как пользоваться?
1. Перейти по ссылке: https://vmrfriz.github.io/bitrix24-rest-swagger/
2. Ввести префикс портала в поле `portal`. Например, для портала `myflower.bitrix24.ru` префиксом будет часть `myflower`
3. Ввести `user_id` и `token` в соответствующие поля.
4. Использовать метод /profile, чтобы убедиться, что доступ к API есть.
   Ответ должен быть примерно следующим:
   ```json
   {
     "result": {
       "ID": "1",
       "ADMIN": true,
       "NAME": "Иван",
       "LAST_NAME": "Иванов",
       "PERSONAL_GENDER": "M",
       "PERSONAL_PHOTO": "https://cdn-ru.bitrix24.ru/b00000000/main/000/000a00aaa0aaa0000a0a00000000aaa0/a00000a0a0000a00a0aaa0aa0aa0a000.jpg",
       "TIME_ZONE": "",
       "TIME_ZONE_OFFSET": 10800
     },
     "time": {
       "start": 1686767881.925928,
       "finish": 1686767881.988622,
       "duration": 0.06269383430480957,
       "processing": 0.010548830032348633,
       "date_start": "2023-06-14T21:38:01+03:00",
       "date_finish": "2023-06-14T21:38:01+03:00",
       "operating_reset_at": 1686768481,
       "operating": 0
     }
   }
   ```

## Как получить токен API
1. Зайти на свой портал, перейти в меню "Разработчикам" - "Другое" - "Входящий вебхук" ()
2. Вверху нажать на карандаш, установить название для токена (не обязательно)
3. В блоке "Настройка прав" дать права для модули, доступ к которым нужно получить по API
4. Скопировать ID пользователя и токен из адреса в поле "Вебхук для вызова rest api" (по шаблону ниже)
   `https://portal.bitrix24.ru/rest/{ID}/{TOKEN}/`
5. Нажать "Сохранить"

## Планы
- [x] Развернуть страницу со Swagger на Github Pages
- [ ] Переносить методы из [официальной документации](https://dev.1c-bitrix.ru/rest_help/general/index.php) в формат openapi

## Ошибки и пожелания
Пожелания, подсказки по структуре файла и об ошибках [пишите в issues](https://github.com/vmrfriz/bitrix24-rest-swagger/pulls).
