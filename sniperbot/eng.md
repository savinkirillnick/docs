# Sniperbot

### Link to download

`http://funnymay.com/products.php`

### Updates

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
Binance
Huobi
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
