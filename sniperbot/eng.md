# Sniperbot

### Link to download

`http://funnymay.com/products.php`

### Updates

#### 2.1.4
* Update API
* Update scroll bar
* Update exchanges list
* Messenger disabled

#### 2.1.3
* Update API

#### 2.1.2
* Update API Kucoin
* Debugging rounds

#### 2.1.1
* Rewrote function for connecting API exchanges
* Fixed updating a position when there are not enough funds on the balance for transactions

#### 2.1
* Rewritten bot engine. Based on Stepbot 2.1
* Settings can be saved to a string and shared
* Added telegram alert function
* Added the function of collecting statistics about transactions
* Fixed display of decimal numbers
* Separated files for storing settings and technical information
* Added new exchanges
* Added Logs

#### 1.2.2
* Fixed rounding of volume before submitting orders to Binance

#### 1.2.1
* Fixed minor errors in scripts working with API Bithumb, Dovewallet, Okex

#### 1.2
* Code update
* Added the ability to change the strategy from outside
* Rewritten functions for storing and outputting logs
* Fixed option to pause purchase after sale

#### 1.1 build 4
* Rounding prices method for Tidex fixed
* Added exchange Kucoin
* Prices calculation function fixed

#### 1.1 build 3
* Pause time function fixed

#### 1.1 build 2
* Rewrited main loop function
* Fixed timings for exchanges API
* Added exchanges Yobit, Livecoin

#### 1.1 build 1
* Minor fixes of exchanges API scripts

#### 1.1
* Added error codes
* Added position module
* Added Cex exchange
* Optimized work by API for Binance, Bithumb, Okex, Dovewallet

#### 1.0 built 5
* Added debug mode. Used with flags -d or --debug
* Change trading start time when bot cancel orders
* Added Bithumb exchange

#### 1.0 build 4
* Added display of time in the logs
* Fixed order cancellation method for Binance
* Minor code optimization
* Added Dovewallet and Tidex exchanges

#### 1.0 build 3
* Added Okex exchange
* Rewritten Huobi orders history display script

#### 1.0 build 2
* Added Exmo exchange
* Rewritten order cancellation script

#### 1.0 build 1
* Working version of Sniperbot

### Description of the program

The program is designed for automatic trading at depth prices.

The bot places purchase orders at the price `bid` + `step`, if the price has fallen below the maximum purchase price `max_buy`

The bot places sell orders at the price of `ask` - `step`, if the price has risen above the minimum selling price of `min_sell`

After checking the parameters, the bot sends a buy or sell order, in accordance with the prices received

### Description of parameters

`Share` - Funnymay passkey (if you do not have a key, enter the word demo to activate in demo mode)

`Init` - Program activation button

`Save` - Save settings button (for full mode)

`Load` - Button for loading settings (for full mode)

`Key` - field for entering the public API key from the exchange

`Secret` - field for entering the secret API-key from the exchange

`Exchange` - Exchange selection

`Set` - field for entering the number of the set of settings (for full mode)

`Max Buy` - Maximum purchase price

`Min Sell` - Minimum sale price

`Step Size` - Step size with which the bot will send orders (see below)

`Lot Size` - Lot size, in the quoted currency, which the bot will trade (for the btc_usdt pair, this is the size of USDT)

`Pair` - field for entering the name of the pair (entered in lowercase through the underscore 'btc_usdt', 'eth_btc', etc.)

`Order Life` - Order lifetime, seconds

`Pause` - Delay time from receiving a signal to sending an order (if you put a negative value, then the time until the candle closes), seconds

`Upd Time` - Delay time between sending requests to the exchange, seconds

`Fee` - the size of the exchange commission, in percent

`Apply` - Button for applying settings and starting the calculation program

`Start` - Button to start the bot (the bot starts to trade)

`Stop` - bot stop button (bot stops trading)

### Description of parameters

The bot supports the following exchanges:
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

#### Parameter Step Size
Value       |Description
------------|-----------------
0           |Sending purchase orders at the best ask price. Sending orders for sale at the best bid price.
Over 0      |Sending purchase orders above the bid price by step. Sending orders to sell below the ask price by step.
Less than 0 |Sending buy orders below the bid price by step. Sending orders to sell above the ask price by step. (inside the spread)

#### Pause parameter
Value       |Description
------------|----------------
0           |Sending orders at the time of receiving a signal
Over 0      |Sending orders after N seconds after receiving a signal
Less than 0 |Sending orders at the time of receiving a signal
