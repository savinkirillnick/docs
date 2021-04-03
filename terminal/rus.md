# Терминал

### Ссылка на скачивание

`http://funnymay.com/products.php`

#### 2.1.1
* Переписана функция подключения API бирж
* Исправлено обновление позиции при наличии средств на балансе не достаточных для сделок

#### 2.1
* Переписан движок бота. За основу взят Stepbot 2.1
* Настройки можно сохранить в строку и поделиться ей
* Добавлена функция оповещения по telegram
* Добавлена функция сбора статистики о сделках
* Исправлено отображение дробных чисел
* Разделены файлы хранения настроек и технической информации
* Добавлены новые биржи
* Добавлены Логи

#### 1.0.2
* Исправлено округление объему перед отправкой ордеров для Binance

#### 1.0.1
* Исправлены мелкие ошибки скриптов работы с API Bithumb, Dovewallet, Okex

#### 1.0
* Рабочая версия программы terminal

### Описание работы программы

Программа представляет собой торговый терминал для ручной торговли.

Терминал позволяет отправлять limit-ордера на покупку и продажу по заданным ценам и объемам.

### Описание параметров

`Share` - Ключ доступа Funnymay (если ключа у вас нет введите слово demo для активации в демо-режиме)

`Init` - Кнопка активации программы

`Save` - Кнопка сохранения настроек (для полного режива)

`Load` - Кнопка загрузки настроек (для полного режима)

`Key` - Поле для ввода открытого API-ключа от биржи

`Secret` - Поле для ввода секретного API-ключа от биржи

`Exchange` - Выбор биржи

`Set` - Поле для ввода номера набора настроек (для полного режима)

`Pair` - Поле для ввода наименование пары (вводится в нижнем регистре через нижнее подчеркивание 'btc_usdt', 'eth_btc' и т.д.)

`Order Life` - Время жизни ордера, секунды

`Upd Time` - Время задержки между отправки запросов на биржу, секунды

`Apply` - Кнопка применения настроек и запуска цикла пограммы

### Биржи

Терминал поддерживает следующие биржи:
```
AAX
ACX
AOFEX
Bequant
Bibox
BigONE
Binance
BinanceUS
Bit2C
bitbank
BitBay
bitcoin.com
Bitfinex
Bitforex
Bitget
Bithumb
bitkk
BitMart
BitMax
BitMEX
Bitpanda Pro
Bitso
Bittrex
Bitvavo
Bit-Z
BL3P
Bleutrade
BTC-Alpha
BtcBox
BTC Trade UA
BW
Bybit
ByteTrade
CDAX
Cex
ChileBit
Coinbase
Coinbase Prime
Coinbase Pro
coincheck
CoinEgg
CoinEx
CoinFalcon
coinfloor
CoinOne
CoinSpot
CREX24
Currency.com
Delta Exchange
Deribit
DigiFinex
EQUOS
Eterbase
Exmo
EXX
FoxBit
FTX
Gate.io
Gemini
GOPAX
HBTC
hitbtc
HollaEx
Huobi Japan
Huobi Pro
IDEX
Independent Reserve
INDODAX
itBit
Kraken
Kucoin
Kuna
LakeBTC
Latoken
LBank
Liquid
Lykke
MixCoins
NDAX
NovaDAX
OceanEx
OKCoin
Okex
Paymium
Phemex
Poloniex
ProBit
qTrade
RightBTC
SouthXchange
STEX
SurBitcoin
TheRockTrading
Tidex
TimeX
Upbit
VBTC
VCC Exchange
Waves.Exchange
WhiteBit
Xena Exchange
Yobit
Zaif
ZB
```
