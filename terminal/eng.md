# Terminal

### Link to download

`http://funnymay.com/products.php`

### Updates

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

#### 1.0.2
* Fixed rounding of volume before submitting orders to Binance

#### 1.0.1
* Fixed minor errors in scripts working with API Bithumb, Dovewallet, Okex

#### 1.0
* Working version of terminal

### Description of the program

The program is a trading terminal for manual trading.

The terminal allows you to send limit buy and sell orders at specified prices and volumes.

### Description of parameters

`Share` - Funnymay passkey (if you do not have a key, enter the word demo to activate in demo mode)

`Init` - Program activation button

`Save` - Save settings button (for full mode)

`Load` - Button for loading settings (for full mode)

`Key` - field for entering the public API key from the exchange

`Secret` - field for entering the secret API-key from the exchange

`Exchange` - Exchange selection

`Set` - field for entering the number of the set of settings (for full mode)

`Pair` - field for entering the name of the pair (entered in lowercase through the underscore 'btc_usdt', 'eth_btc', etc.)

`Order Life` - Order lifetime, seconds

### Exchanges

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
