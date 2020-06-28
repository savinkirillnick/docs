# Stepbot

### Link to download

`http://funnymay.com/products.php`

#### 0.1 beta
* Beta version of stepbot

### Description of the program

First, the bot calculates the initial price - the maximum price since the bot was launched. If the price starts to fall, then the bot starts to be purchased in steps that it will calculate, in accordance with the parameters that we entered.

Each next step can be cleared with a change in the size of the price step and a change in the size of the step of the lot amount.

The bot recalculates the position size for each transaction - calculates the average price of the position and the amount.

The sales step is also calculated. The bot can sell in steps, or all at once.

When the price changes direction and starts to go up, the bot closes the position and re-calculates the initial price.

The bot works both on an uptrend and a downtrend.

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

`Pause` - Delay time from receiving a signal to sending an order (if you put a negative value, then the time until the candle closes), seconds

`Upd Time` - Delay time between sending requests to the exchange, seconds

`Depo` - Deposit allocated for the purchase

`Num Step` - Number of sales steps

`Buy from` - A parameter that shows what price to start building each next step from. From the initial price or from the last transaction price.

`Sell from` - Parameter showing at what price to start building each next step. From the starting price, the average price of a position, or from the last transaction price.

`Step type` - A type indicating in which units to calculate the price step. In absolute prices or as a percentage of the price

`Step Size` - Size of the price step (in points or percent, i.e. at a price of 9800 - 10 points means that the step will be at a price of 9790, and 10 percent means that the step will be at a price of 8820)

`Step ratio` - The coefficient of increase / decrease in the price step. Each subsequent trade, the price step size will be multiplied by a given coefficient (for example, for a pair of BTC / USDT with a step of 10 points and a coefficient equal to 2.0, the first step will be 10 USDT lower, the second step 20 USDT lower, the third 40 USDT lower, the fourth one 80 USDT etc.)

`Lot type` - A type indicating in which units to calculate the step amount.

`Lot Size` - Size of the step amount (indicated in quoted currency, i.e. for the BTC / USDT pair we indicate how much USDT we spend per step. BTC is calculated automatically)

`Lot ratio` - Increase / decrease ratio of the step amount. Every subsequent trades, the size of the step amount will be multiplied by a given coefficient

### Description of parameters

The bot supports the following exchanges:
```
Binance
Bithumb
Dovewallet
Cex
Exmo
Huobi
Livecoin
Okex
Tidex
Yobit
```
