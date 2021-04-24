# Отчёт о тестировании <KeyValidator.class>

## Краткий результат

Целью тестирования стали две документации: 
 - Инструкция по установке OpenJDK 11;
 - Руководство использования.
 
 В документации "Инструкция по установке OpenJDK 11" не было совершенно ошибок. Установка по инструкции на ОС прошла успешно. Во второй документации (Руководство использования) были допущены ошибки в примерах, как вводить ключ для проверки, а также ключи представленные, как "валидные" и "невалидные".

15.03.21> - <15.03.21 было проведено тестирование документации, функциональное тестирование приложения <KeyValidator.class>.

На тестирование затрачено: <40 минут>

В результате тестирования выявлены следующие дефекты:
* [#1 Приложение KeyValidator не принимает при вводе валидный ключ VISA](https://github.com/ZmbOrk/Homework-1.1---2-Java/issues/1)
* [#2 В руководстве пользователя к приложению KeyValidator указан некорректный валидный ключ](https://github.com/ZmbOrk/Homework-1.1---2-Java/issues/2)
* [#3 В руководстве пользователя к приложению KeyValidator некорректный пример](https://github.com/ZmbOrk/Homework-1.1---2-Java/issues/3)
* [#4 Приложение KeyValidator при вводе 19-ти символьной карты VISA сообщает об ошибке](https://github.com/ZmbOrk/Homework-1.1---2-Java/issues/4)

## Описание процесса тестирования

### В качестве тестовых данных использовались данные с [источника "Руководство пользователя"](https://github.com/netology-code/javaqa-homeworks/blob/master/intro/user-manual.md):
*Валидные ключи: 
- 8f05e6a7-70e9-33d7-bfe7-b19eae0d8998б
- 80b427f8-92cd-3aae-ba04-3927fbe17c6
- b295bc63-9f03-3b4b-af80-969b39f8c262
- 387eedc6-12e9-3b32-9881-63b6b5e85317
- c19a8cf9-5c3a-37c5-b7f3-d16d38a0c180
 С ожидаемым результатом "Result for ... OK" 

*Невалидные ключи: 
- 18252235-78e0-44a5-8720-556f0c7da17a;
- e66075b6-ddad-445e-baf6-161b3289522b;
- b6d53250-f07e-4352-a293-6102ddf7f1ca;
- c2bc778a-1cb9-46c6-b435-0489649d2a42;
- 2fb98b44-93e7-3bdd-a2ad-79347bfe4ad 
С ожидаемым результатом "Result for ... FAIL"

### Предоставленные данные из примера [источника "Руководство пользователя"](https://github.com/netology-code/javaqa-homeworks/blob/master/intro/user-manual.md):
- 00000000-0000-0000-0000-000000000000
- 00000000-0000-0000-0000-000000000001 
с ожидаемым результатом 
Result for 00000000-0000-0000-0000-000000000000: OK
Result for 00000000-0000-0000-0000-000000000001: FAIL

### Предоставленные данные из сайта генератора -  https://www.getcreditcardnumbers.com/
- 44853295-1295-0564-465 
- 4485329512950564465 
C ожидаемым результатом: "Вы ввели неверные данные для проверки ключа"

В приложении KeyValidator по очередно вводились данные, согласно инструкции. 


Тестирование производилось в следующем окружении:
* <Win10, 64x>
* <Java 8, Java 10.0.10>
* <Git Bash, GitHub>  
