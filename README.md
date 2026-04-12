# creditcard

A simple class for identifying, validating, and formatting credit card numbers.

> **Maintained fork** of [alexforster/creditcard](https://github.com/alexforster/creditcard).  
> Changes: dropped `pkg_resources` dependency (fixes Python 3.12+), modernized packaging to `pyproject.toml`.

## Install

```bash
pip install pycreditcard
```

## Usage

```python
from creditcard import CreditCard

card = CreditCard('4111111111111111', expire_month='03', expire_year='2030', code='123')
print(card.brand)    # Visa
print(card.is_valid) # True
```

### Supported Card Families

**Note:** pull requests for [new cards](creditcard/data/registry.xml) are welcome!

 * Visa
 * American Expiress
 * Mastercard
 * Discover
 * Diners Club
 * UnionPay (China)
 * JCB (Japan Credit Beauro)


## Changes from Original

| Version | Change |
|---|---|
| 1.1.0 | Replaced `pkg_resources` with `importlib.resources` (Python 3.12+ fix) |
| 1.1.0 | Migrated packaging to `pyproject.toml` |

## Credits

Original library authored by [Alex Forster](https://github.com/alexforster).  
Copyright 2017 Alex Forster. All rights reserved.  
Licensed under the [MIT License](LICENSE).