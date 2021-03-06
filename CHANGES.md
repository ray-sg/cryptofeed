## Changelog

### 0.18.0
  * Feature: InfluxDB support via backend

### 0.17.4 (2018-11-17)
  * Readme change for long description rendering issue

### 0.17.3 (2018-11-17)
  * Feature #41: Rework trading pairs to generate them dynamically (as opposed to hard coded)
  * Feature: When book depth configured Redis, ZMQ and UDP backends only report book changes when changed occurred in 
             depth window
  * Feature: TCP socket backend support
  * Feature: UDS backend support

### 0.17.2 (2018-11-03)
  * Bugfix #45: Bitstamp prices and sizes in L2 book are string, not decimal.Decimal
  * Feature: Binance support

### 0.17.1 (2018-10-19)
  * Bugfix #43: Coinbase L2 book used "0" rather than 0 for comparisons against decimal.Decimal
  * Feature: REST feed market data supported via normal subscription methods
  * Feature: Kraken support
  * Bugfix: Bitfinex book timestamps match expected bitfinex timestamps (in ms)

### 0.17.0 (2018-10-13)
  * Feature: Timestamps for orderbooks and book deltas
  * Feature #40: NBBO now uses best bid/ask from L2 books
  * Feature #28: GDAX now renamed Coinbase and uses coinbase endpoints
  * Feature: ZeroMQ backend. Write updates directly to zmq connection
  * Feature: UDP Socket backend. Write updates directy to UDP socket

### 0.16.0 (2018-10-4)
  * Feature: L2 books are now all price aggregted amounts, L3 books are price aggregated orders
  * Book deltas supported on all feeds
  * Bugfix: Fix NBBO feed

### 0.15.0 (2018-09-29)
  * Feature: GDAX/Coinbase rest support - trades, order status, etc
  * Feature: Arctic backend, supports writing to arctic directly on trade/funding updates
  * Bugfix: #36 Update poloniex to use new trading pairs and handle sequence numbers
  * Bugfix: Improve Bitfinex orderbooks and handle sequence numbers
  * Bugfix: GDAX and Bitmex orderbook and logging improvements

### 0.14.1 (2018-09-14)
  * Added some docstrings
  * Feature: Add exchanges by name to feedhandler. Easier to instantiate a feedhandler from config
  * Logging improvements
  * Bugfix: non-gathered futures were suppressing exceptions when multiple feeds are configured. Changed to tasks 
  * Redis backend uses a connection pool

### 0.14.0 (2018-09-04)
  * Feature: support for writing order books directly to redis
  * Feature: ability to specify book depth for redis updates

### 0.13.3 (2018-08-31)
  * Feature: normalize bitfinex funding symbols

### 0.13.2 (2018-08-31)
  * Bugfix: fix symbol in bitfinex rest

### 0.13.1 (2018-08-31)
  * Feature: access rest endpoints via getitem / []
  * Bugfix: #31 - funding channel broke gemini
  * Feature: Book deltas for GDAX
  * Bugfix: Fix intervals on Bitmex (rest)

### 0.13.0 (2018-08-22)
  * Feature: Funding data from Bitmex on ws
  * Feature: Funding historical data via rest
  * Bugfix: Python 3.7 compatibility
  * Feature: Rest trade APIs are now generators
  * Feature: funding data on bitfinex - ws and rest

### 0.12.0 (2018-08-20)
  * Bugfix: Handle 429s in Bitmex (REST)
  * Feature: Redis backend for trades to write updates directly to redis
  * Bugfix: issue #27 - Bitmex trades missing timestamps

### 0.11.1 (2018-08-18)
  * Bitfinex and Bitmex historical trade data via REST
  * Bugfix: interval incorrect for rest time ranges
  * Bugfix: lowercase attrs in Rest interface

### 0.11.0 (2018-08-05)
  * Feature: Support for delta updates for order books
  * REST api work started

### 0.10.2
  * Bugfix: Clear data structures on reconnect in bitmex
  * Feature: Support reconnecting on more connection errors
  * Feature: Timestamp support on trade feeds
  * Feature: Connection watcher will terminate and re-open idle connections

### 0.10.1 (2018-5-11)
  * Feature: Reconnect when a connection is lost
  * Bugfix #22: Check for additional connection failures
  * Feature #4: Trade ID support
  * Feature: Account for new gemini message type

### 0.10.0 (2018-03-18)
  * Feature: Bitmex

### 0.9.2 (2018-03-13)
  * Bugfix #10: Change from float to decimal.Decimal in GDAX
  * Feature #5: use sorted dictionaries for order books
  * Feature #17: logging support
  * Bugfix: Gemini order books now work
  * Bugfix: All json floats parsed to Decimal
  * Bugfix: Fix Bitstamp pair parsing
  * Feature: Major clean up of channel, exchange, and trading pair names

### 0.9.1 (2018-01-27)
  * Bugfix #4: produce ticker from trades channel on GDAX
  * Feature: Bitstamp feed

### 0.8.0 (2018-01-07)
  * Feature: HitBTC feed
  * Feature: Poloniex Orderbook support

### 0.6.0 (2018-01-02)
  * Feature: Gemini Feed

### 0.5.0 (2018-01-02)
  * Initial release: GDAX, Poloniex, Bitfinex Support
  * Feature: NBBO support
