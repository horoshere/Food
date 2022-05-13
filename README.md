# Food
Работа с JS на готовом макете.
https://food.horoshere.ru/

С помощью **нативного javascript** выполнен функционал:
* Переключения табов
* Слайдер
* Калькулятор расчета калорий
* Модальные окна
* Реализация таймера на странице
* Работа с технологиями **AJAX** и **Promise**


## Особенности
1. В блоке *Калькулятор калорий* выбранные данные сохраняются в **localStorage**.  
![localstorage](https://sun9-24.userapi.com/s/v1/ig2/ihUQifin6AvMgYp9_2TPg5PabvN3akc-CCcMljB9Eg278optA_OnC0CG4G7sOWNmocn8ZXkl88n0TC-GU9ZWi1LM.jpg?size=640x227&quality=96&type=album)


2. Создан локальный сервер с помощью [json-server - npm](https://www.npmjs.com/package/json-server) и [db.json](https://github.com/horoshere/Food/blob/main/dist/db.json).


3. Блок *Наше меню на день* создан с помощью **Классов**.  
![menuCards](https://sun9-17.userapi.com/s/v1/ig2/1dAG4cPs5IshFWT3TOJFAK9ano77utSRCnKjIXv-DLyxDlX4IUDADK8V2E2ffl-_XvYoiCdP1uefGS8TijRIDzwN.jpg?size=784x401&quality=96&type=album)  

Данные для карточек получены с сервера [db.json](https://github.com/horoshere/Food/blob/main/dist/db.json).

```js
//js code
getContent('http://localhost:3000/menu')
        .then(data => {
            data.forEach(({img, altimg, title, descr, price}) => {
                new MenuCard(img, altimg, title, descr, price, '.menu .container').render();
            });
        });
```

4. Заполненные данные из *Форм* постятся на сервер.  

![requests](https://sun9-60.userapi.com/s/v1/ig2/rb9bkTgAdmdVaSmqwJtEO-1josJFXu8FNRN8xOVl8rDnalQm4bjfq0-DEf_X4bZtt2klGGAbn72GPKZ2bph8M5zo.jpg?size=337x370&quality=96&type=album)


