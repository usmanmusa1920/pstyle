# Pycss

Pycss it is python text-style ✅ not python textile! 🤔 it actually print your text on terminal in different kind of colors.

[![Downloads Month Badge](https://static.pepy.tech/badge/pycss/month)](https://pypi.org/project/pycss)
[![Downloads Week Badge](https://static.pepy.tech/badge/pycss/week)](https://pypi.org/project/pycss)
[![License Badge](https://img.shields.io/pypi/l/pycss.svg)](https://pypi.org/project/pycss)
[![Supported Wheel Badge](https://img.shields.io/pypi/wheel/pycss.svg)](https://pypi.org/project/pycss)
[![Supported Versions Badge](https://img.shields.io/pypi/pyversions/pycss.svg)](https://pypi.org/project/pycss)
[![Contributors](https://img.shields.io/github/contributors/usmanmusa1920/pycss.svg)](https://github.com/usmanmusa1920/pycss/graphs/contributors)

# Simple use of pycss

First we recommend creating a virtual environment `python -m venv venv` and then activate it `source venv/bin/activate`

Once that finish now install the library using

```sh
    pip install pycss
```

Wait for the installation to finish, basically the library was uploaded using `sdist` (Source Distribution) and `bdist_wheel` (Built Distribution).

To print text with color using python print, instead of using `print` function, use any of the following functions (purple, blue, cyan, green, yellow, red, normal, bold, underline, log_style)

```python
    >>> from pycss import (purple, blue, cyan, green, yellow, red, normal, bold, underline)

    >>> purple('I am purple in color')
    >>> blue('I am blue in color')
    >>> cyan('I am cyan in color')
    >>> green('I am green in color')
    >>> yellow('I am yellow in color')
    >>> red('I am red in color')
    >>> normal('I am a normal text')
    >>> bold('I make text bold')
    >>> underline('I underline text')
```

To print logging text with color:

```python
    >>> import logging
    >>> from pycss import log_style
    
    >>> FORMATTER = '[+] [%(asctime)s] [%(levelname)s] %(message)s'
    >>> logging.basicConfig(format=FORMATTER)
    >>> LOGGER = logging.getLogger(__name__)
    >>> LOGGER.setLevel(logging.DEBUG)

    >>> log_style('I am info logger')
    >>> log_style('I am yellow logger', col='yellow')
    >>> log_style('I am error logger', log='error')
```

See more documentations <a href="https://pycss.readthedocs.io">here!</a>

## Useful links

-   Documentation: https://pycss.readthedocs.io
-   Repository: https://github.com/usmanmusa1920/pycss
-   PYPI Release: https://pypi.org/project/pycss

Pull requests are welcome
