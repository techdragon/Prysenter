=========
Prysenter
=========

Prysenter is an absolutely minimal, text-only, terminal-only presentation runner.
It shows a sequence of strings, centered in your terminal.

----------
Installing
----------
Download and run presenter.py for an example of what it looks like.

The python module, `colorama <http://pypi.python.org/pypi/colorama>`_, is an optional dependency for colorized output of slides.

Color Mappings
--------------

* f_color maps to colorama.Fore.CODE constant.
* b_color maps to colorama.Back.CODE constant.
* s_color maps to colorama.Style.CODE constant.

A code example is in the Usage section below.

-----
Usage
-----
Crank the font size on your terminal, run your presentation.

New Presentations
-----------------

::

    from prysenter import Prysentation
    slides = ['Intro to Prysenter',
              'Prysenter presents',
              'Simple',
              'Minimal',
              'Quick',
              'Thank You.',]
    Prysentation(slides=slides).start()


Color Example
-------------

::

    from prysenter import Prysentation
    slides = ["{f_red}Red Slide",
              "{f_green}Slide",
              "{b_white}{f_yellow}{s_bright}What is this, I don't even.{s_reset_all}"]
    Prysentation(slides=slides).start()

Timeout Example
---------------
You can make all your slides advance after a presentation-wide timeout:

::

    from prysenter import Prysentation, pechakucha
    slides = ["Pecha",
              "Kucha",
              "Who would ever need more",
              "Than 20 Seconds?"]
    Prysentation(slides=slides, timeout=pechakucha.timeout).start()

