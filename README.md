[![Build Status](https://travis-ci.org/husl-colors/husl-python.svg?branch=master)](http://travis-ci.org/husl-colors/husl-python)
[![Package Version](https://img.shields.io/pypi/v/husl.svg)](https://pypi.python.org/pypi/husl/)

A fork of the Python implementation of [HUSL](http://www.husl-colors.org) (revision 3).

This fork uses numpy instead of math for calcution and accepts numpy arrays for the color channels. Original scalar functions are still available but prefixed with **_sc_**. Ideal would be to reimplement them as numpy ufuncts using C.

## Installation

`pip install husl` or `python setup.py install --user`

## Usage

**husl_to_hex(hue, saturation, lightness)**

`hue` is a float between 0 and 360, `saturation` and `lightness` are floats or numpy arrays between 0 and 100. This function returns the resulting color as a hex string.

**husl_to_rgb(hue, saturation, lightness)**

Like above, but returns a list of 3 floats or arrays between 0 and 1, for each RGB channel.

**rgb_to_husl(red, green, blue)**

Like above, but `red`, `green` and `blue` are passed as floats between 0 and 1.

For HUSLp (the pastel variant), use `huslp_to_hex`, `huslp_to_rgb`, `hex_to_huslp` and `rgb_to_huslp`.

**complex_to_rgb(z, amin, amix, mode='special', ...)**

Converts complex array to an RGB representation, mapping phase to hue and modulus to some form of lightness, depending on the chosen mode. For detailed paramter description, look at the docs of the function

## Testing

Run `python setup.py test`.

## Authors

* Robert McGinley ([mcginleyr1](http://github.com/mcginleyr1))
* Alexei Boronine ([boronine](http://github.com/boronine))
* Bjoern Enders ([bjoernenders](http://github.com/bjoernenders))
