
RGBpy
#####

RGBpy it is python text-style ✅ not python textile! 🤔 it actually print your text on terminal in different kind of colors, including logging.

Release v\ |version|


.. image:: https://static.pepy.tech/badge/rgbpy/month
    :target: https://pepy.tech/project/rgbpy
    :alt: RGBpy Downloads Per Month Badge

.. image:: https://static.pepy.tech/badge/rgbpy/week
    :target: https://pepy.tech/project/rgbpy
    :alt: RGBpy Downloads Per Week Badge
    
.. image:: https://img.shields.io/pypi/l/rgbpy.svg
    :target: https://pypi.org/project/rgbpy/
    :alt: License Badge

.. image:: https://img.shields.io/pypi/wheel/rgbpy.svg
    :target: https://pypi.org/project/rgbpy/
    :alt: Wheel Support Badge

.. image:: https://img.shields.io/pypi/pyversions/rgbpy.svg
    :target: https://pypi.org/project/rgbpy/
    :alt: Python Version Support Badge

.. image:: https://img.shields.io/github/contributors/usmanmusa1920/rgbpy.svg
    :target: https://github.com/usmanmusa1920/rgbpy/graphs/contributors
    :alt: Contributors Badge
    
-------------------

Simple use of rgbpy
===================

First we recommend creating a virtual environment **python -m venv venv** and then activate it **source venv/bin/activate**

Once that finish now install the library using::

    pip install rgbpy
    
Wait for the installation to finish, basically the library was uploaded using `sdist` (Source Distribution) and `bdist_wheel` (Built Distribution).

.. code-block:: python

    # To print text with color using python print, instead of using `print` function, use any of the following functions (purple, blue, cyan, green, yellow, red, normal, bold, underline, log_style)

    >>> from rgbpy import (purple, blue, cyan, green, yellow, red, normal, bold, underline)

    >>> purple('I am purple in color')
    >>> blue('I am blue in color')
    >>> cyan('I am cyan in color')
    >>> green('I am green in color')
    >>> yellow('I am yellow in color')
    >>> red('I am red in color')
    >>> normal('I am a normal text')
    >>> bold('I make text bold')
    >>> underline('I underline text')

    # To print logging text with color
    
    >>> import logging
    >>> from rgbpy import log_style
    
    >>> FORMATTER = '[+] [%(asctime)s] [%(levelname)s] %(message)s'
    >>> logging.basicConfig(format=FORMATTER)
    >>> LOGGER = logging.getLogger(__name__)
    >>> LOGGER.setLevel(logging.DEBUG)

    >>> log_style('I am info logger')
    >>> log_style('I am yellow logger', col='yellow')
    >>> log_style('I am error logger', log='error')


RGBpy with print
=================

Using rgbpy `purple` `blue` `cyan` `green` `yellow` `red` `normal` `bold` or `underline` function, give your print text beautiful color that you want.

Use `purple` function to make text purple in color::
    
    purple('I am purple in color')

Use `blue` function to make text blue in color::
    
    blue('I am blue in color')

Use `cyan` function to make text cyan in color::
    
    cyan('I am cyan in color')

Use `green` function to make text green in color::
    
    green('I am green in color')

Use `yellow` function to make text yellow in color::
    
    yellow('I am yellow in color')

Use `red` function to make text red in color::
    
    red('I am red in color')

Use `normal` function to make text normal in color::
    
    normal('I am a normal text')

Use `bold` function to make text bold in color::
    
    bold('I make text bold')

Use `underline` function to make text underline in color::
    
    underline('I underline text')


RGBpy with logging
==================

RGBpy `log_style` function give your logging text beautiful color that you want. When using `log_style` construct your logger formatter, setLevel to your need, then call the log_style function with the text you want it to display. Example when using logging without rgbpy, it could be set like this:

.. code-block:: python

    import logging

    FORMATTER = '[+] [%(asctime)s] [%(levelname)s] %(message)s'
    logging.basicConfig(format=FORMATTER)
    LOGGER = logging.getLogger(__name__)
    LOGGER.setLevel(logging.DEBUG)

    # log text
    LOGGER.info('I am info logger')

The equivalent of the above using rgbpy `log_style` function is:

.. code-block:: python

    import logging
    from rgbpy import log_style

    FORMATTER = '[+] [%(asctime)s] [%(levelname)s] %(message)s'
    logging.basicConfig(format=FORMATTER)
    LOGGER = logging.getLogger(__name__)
    LOGGER.setLevel(logging.DEBUG)

    # log text
    log_style('I am info logger')

By default, the default logging is `info`, but user will be able to change it by passing `log` kwargs and give it the value of the logging (set log level) he/she want, e.g:

.. code-block:: python
    
    # error log
    log_style('I am error logger', log='error')

The color set for:

`info` log is `green`

`yellow` log is `yellow`

`error` log is `red`

`critical` log is `cyan`

If the kwargs value of (log) is not (info, yellow, error, or critical) log color is `magenta`

With all these log that have their own default colors, it can also be change. Example, let log an error message by changing the color text to green:

.. code-block:: python

    log_style('I am error log, but green in color bold txt', log='error', col='green')

Also, a text can be also set to be bold by including `bold` positional argument:

.. code-block:: python

    log_style('I am error log, but green in color, also with  bold txt', 'bold', log='error', col='green')

This two are thesame (inter-changebly), (use if text need to be bold)

.. code-block:: python

    log_style('I am error log of cyan(color) bold txt', 'cyan', log='error', col='bold')
    log_style('I am error log of cyan(color) bold txt', 'bold', log='error', col='cyan')


Useful links:
-------------

- `Repository <https://github.com/usmanmusa1920/rgbpy>`_

- `PYPI Release <https://pypi.org/project/rgbpy>`_
