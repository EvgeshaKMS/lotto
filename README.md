# Тестовое задание

## Требуется реализовать логику игры.

### Правила следующие:

У игры есть два поля, в первом поле будет девятнадцать клеток, во втором две клетки. От участника лотереи требуется отметить в первом поле восемь цифр, во втором одну цифру. При вычисление результата потребуется сравнить отмеченные участником числа с двумя случайно сгенерированными, в соответствиями с правилами игры (восемь чисел в первом массиве, одно во втором массиве), массивами чисел. В случае совпадения четырех и более цифр в первом поле, либо трех и более чисел в первом поле и одного во втором, пользователь считается победителем лотереи и получает причитающиеся ему лавры (ничего не получает).

- Реализовать генерацию случайно выбранных полей в билете (в соответствие с правилами лотереи) по нажатию на значок волшебной палочки.
- (not yet implemented) Реализовать логику отправки выбранных чисел на сервер по любому url'у (предлагаем использовать фейковый url, чтобы не иметь дела с CORS). Отправка должна происходить после нажатия на кнопку "Показать результат". В данных отправки должен быть объект

    ```
    {
        selectedNumber: {
            firstField: number[];
            secondField: number[]
        };
        isTicketWon: boolean;
    }
    ```

    Нужно предусмотреть ситуацию, что в ответ придет код ответ не 200 OK, а любой другой. В таком случае требуется отправлять запрос еще два раза с интервалом 2 секунды. Если ответ 200 OK так и не пришел, то выдать какое-либо уведомление об ошибке.

В качестве референса использовался макет https://www.figma.com/file/VDraSBJhGzDKP33eS4IBbp6Z/Finch_test
