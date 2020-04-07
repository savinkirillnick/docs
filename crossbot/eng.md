# Crossbot

### Link to download

`http://funnymay.com/products.php`

### Updates

#### 1.0 build 3
* Added Huobi exchange
* Extended work with intervals, added `3d`,` 1w`, `1M`
* Bringing the `timestamp` parameters of different functions to uniform values

#### 1.0 build 2
* Added the ability to select different types for fast and slow moving
* Fixed display of `Qty` value (was: 0.049999999999999993, became 0.05)

#### 1.0 build 1
* Added selection of moving average types for Crossbot and Crossbot Research
* Added calculations `SMA`,` WMA`, `SMMA`
* Correction of field switching with the `Tab` button

#### 1.0
* Working version of Crossbot
* Working version of Crossbot Research

### Description of the program

Video instruction `https://youtu.be/mc3e0wIsJng`

The program works on the principle of trading on the intersection of moving averages

Moving with a smaller parameter is called fast moving

Moving with a large parameter is called slow moving

When the fast moving crosses the slow moving from the bottom up, the bot receives a bullish signal - a buy signal

When a fast moving one crosses a slow moving one from top to bottom, the bot receives a bearish signal - a sell signal

After checking the parameters, the bot sends a buy or sell order, in accordance with the received signal

### Description of parameters

`Share` - Funnymay passkey (if you do not have a key, enter the word `demo` to activate in demo mode)

`Init` - Program activation button

`Save` - Save settings button (for full mode)

`Load` - Button for loading settings (for full mode)

`Key` - field for entering the public API key from the exchange

`Secret` - field for entering the secret API-key from the exchange

`Exchange` - Exchange selection

`Set` - field for entering the number of the set of settings (for full mode)

`Fast MA` - Type selection and setting the parameter of fast moving average

`Slow MA` - Type selection and setting the parameter of the slow moving average

`Upd Time` - Delay time between sending requests to the exchange, seconds

`Interval` - Dimension of graphs on which the bot will work (see below)

`Pair` - Field for entering the name of the pair (entered in lowercase through the underscore 'btc_usdt', 'eth_btc', etc.)

`Order Life` - Order lifetime, seconds

`Pause` - Delay time from receiving a signal to sending an order (if you put a negative value, then the time until the candle closes), seconds

`Step Size` - Step size with which the bot will send orders (see below)

`Apply` - Button for applying settings and starting the calculation program

`Start` - Button to start the bot (the bot starts to trade)

`Stop` - Bot stop button (bot stops trading)

### Description of parameters

The bot supports the following exchanges:
```
Binance
Huobi
```

#### Parameter Step Size
Value           |Description
---------------|-----------------------
0              |Sending purchase orders at the best ask price. Sending orders for sale at the best bid price.
Greater than 0 |Sending purchase orders above the ask price by step. Sending orders to sell below the bid price by step.
Less than 0    |Sending buy orders below the ask price by step. Sending sell orders above the bid price by step. (inside the spread)

#### Pause parameter
Value          |Description
---------------|----------------
0              |Sending orders at the time of receiving a signal
Greater than 0 |Sending orders after N seconds after receiving a signal
Less than 0    |Sending orders after receiving a signal and N seconds before the candle closes

#### Interval parameter

Parameters supported by `Binance`
Parameter | Description
--------- | ---------------
1m        |1 minute
3m        |3 minutes
5m        |5 minutes
15m       |15 minutes
30m       |30 minutes
1h        |1 hour
2h        |2 hours
4h        |4 hours
6h        |6 hours
8h        |8 hours
12h       |12 hours
1d        |1 day
3d        |3 days
1w        |1 week
1M        |1 month

Parameters supported by `Huobi`
Parameter | Description
--------- | ---------------
1m        |1 minute
5m        |5 minutes
15m       |15 minutes
30m       |30 minutes
1h        |1 hour
4h        |4 hours
1d        |1 day
1w        |1 week
1M        |1 month
