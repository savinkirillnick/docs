# Кроссбот

### Ссылка на скачивание

`http://funnymay.com/products.php`

### Обновления

#### 1.0 build 3
* Добавлена биржа Huobi
* Расширена работа с интервалами, добавлены `3d`, `1w`, `1M`
* Приведение параметров `timestamp` разных функций к единым величинам

#### 1.0 build 2
* Добавлена возможность выбора разных типов для быстрой и медленной скользящей
* Исправлено отображение значения `Qty` (было: 0.049999999999999993, стало 0.05)

#### 1.0 build 1
* Добавлен выбор типов скользящих средних для Crossbot и Crossbot Research
* Добавлены расчеты `SMA`, `WMA`, `SMMA`
* Коррекция переключения полей кнопкой `Tab`

#### 1.0
* Рабочая версия программы Crossbot
* Рабочая версия программы Crossbot Research

### Описание работы программы

Видео инструкция `https://youtu.be/mc3e0wIsJng`

Программа работает по принципу торговли по пересечению скользящих средних

Скользящая с меньшим параметром называется быстрой скользящей

Скользящая с большим параметром называется медленной скользящей

Когда быстрая скользящая пересекает медленную скользящую снизу-вверх, бот получает бычий сигнал - сигнал на покупку

Когда быстрая скользящая пересекает медленную скользящую сверху-вниз, бот получает медвежий сигнал - сигнал на продажу

После проверок параметров бот посылает ордер на покупку или продажу, в соответствии с полученным сигналом

### Описание параметров

`Share` - Ключ доступа Funnymay (если ключа у вас нет введите слово demo для активации в демо-режиме)

`Init` - Кнопка активации программы

`Save` - Кнопка сохранения настроек (для полного режива)

`Load` - Кнопка загрузки настроек (для полного режима)

`Key` - Поле для ввода открытого API-ключа от биржи

`Secret` - Поле для ввода секретного API-ключа от биржи

`Exchange` - Выбор биржи

`Set` - Поле для ввода номера набора настроек (для полного режима)

`Fast MA` - Выбор типа и установка параметра быстрой средней скользящей

`Slow MA` - Выбор типа и установка параметра медленной средней скользящей

`Upd Time` - Время задержки между отправки запросов на биржу, секунды

`Interval` - Размерность графиков, на которых будет работать бот (см. ниже)

`Pair` - Поле для ввода наименование пары (вводится в нижнем регистре через нижнее подчеркивание 'btc_usdt', 'eth_btc' и т.д.)

`Order Life` - Время жизни ордера, секунды

`Pause` - Время задержки от получения сигнала до отправки ордера (если поставить отрицательное значение, то время до закрытия свечи), секунды

`Step Size` - Размер шага, с которым бот будет отправлять ордера (см. ниже)

`Apply` - Кнопка применения настроек и запуска пограммы обсчета

`Start` - Кнопка запуска бота (бот начинает торговать)

`Stop` - Кнопка остановки бота (бот прекращает торговать)

### Описание параметров

Бот поддерживает следующие биржи:
```
Binance
Huobi
```

#### Параметр Step Size
Значение | Описание
---------|-----------------
0        |Отправка ордеров на покупку по лучшей цене ask. Отправка ордеров на продажу по лучшей цене bid.
Больше 0 |Отправка ордеров на покупку выше цены ask на величину step. Отправка ордеров на продажу ниже цены bid на величину step.
Меньше 0 |Отправка ордеров на покупку ниже цены ask на величину step. Отправка ордеров на продажу выше цены bid на величину step. (внутри спреда)

#### Параметр Pause
Значение |Описание
---------|----------------
0        |Отправка ордеров в момент полученя сигнала
Больше 0 |Отправка ордеров сустя N секунд после получения сигнала
Меньше 0 |Отправка ордеров после получения сигнала и за N секунд до закрытия свечи

#### Параметр Interval

Параметры, которые поддерживает `Binance`
Параметр | Описание
---------|---------------
1m       |1 минута
3m       |3 минуты
5m       |5 минут
15m      |15 минут
30m      |30 минут
1h       |1 час
2h       |2 часа
4h       |4 часа
6h       |6 часов
8h       |8 часов
12h      |12 часов
1d       |1 день
3d       |3 дня
1w       |1 неделя
1M       |1 месяц

Параметры, которые поддерживает `Huobi`
Параметр | Описание
---------|---------------
1m       |1 минута
5m       |5 минут
15m      | 15 минут
30m      |30 минут
1h       |1 час
4h       |4 часа
1d       |1 день
1w       |1 неделя
1M       |1 месяц
