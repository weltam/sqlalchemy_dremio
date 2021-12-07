# SQLAlchemy Dremio


![PyPI](https://img.shields.io/pypi/v/sqlalchemy_dremio.svg)
![Build](https://github.com/narendrans/sqlalchemy_dremio/workflows/Build/badge.svg)

A SQLAlchemy dialect for Dremio via Flight interfaces.

<!--ts-->
   * [Installation](#installation)
      * [Pre-Requisites](#pre-requisites)
   * [Usage](#usage)
      * [Arrow Flight](#arrow-flight)
   * [Testing](#testing)
   * [Superset Integration](#superset-integration)
<!--te-->

Installation
------------

`pip3 install sqlalchemy_dremio`


Usage
------------

Arrow Flight
------
```diff
- This is experiemental. Not recommended for production usage.
```

Connection String example:
`dremio+flight://user:password@host:port/dremio`

Refer https://github.com/dremio-hub/dremio-flight-connector for configuring flight endpoint in Dremio.

Testing
------------

Set the environment variable DREMIO_CONNECTION_STRING:

Linux:
`export DREMIO_CONNECTION_URL="dremio://dremio:dremio123@localhost:31010/dremio"`

And then run:

```sh
export DREMIO_CONNECTION_URL="dremio+flight://welly:dremio123@10.100.0.109:32010/dremio"
```

```py
py.test test
```

Superset Integration
-------------

This SQLAlchemy can be used for connecting Dremio with Superset. Please check superset website for more instructions on the setup.

Development
-------------

```sh
pip install -r requirements_dev.txt
```

build

```sh
sudo python3 setup.py install
```
ref: https://stackoverflow.com/questions/1471994/what-is-setup-py

