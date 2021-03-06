.. delorean documentation master file, created by
   sphinx-quickstart on Tue Jan  8 00:44:25 2013.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.



Delorean: Time Travel Made Easy
==============================

This document describes Delorean v\ |version|.

`Delorean` is a library for clearing up the inconvenient truths that arise dealing with datetimes in Python. Understanding that timing is a delicate enough of a problem `delorean` hopes to provide a cleaner less troublesome solution to shifting, manipulating, generating `datetimes`.

Delorean stands on the shoulders of giants `pytz <http://pytz.sourceforge.net/>`_ and `dateutil <http://labix.org/python-dateutil>`_

`Delorean` will provide natural language improvements for manipulating time, as well as datetime abstractions for ease of use. The overall goal is to improve datetime manipulations, with a little bit of software and philsophy.

Pretty much make you a badass, time traveller.

Getting Started
^^^^^^^^^^^^^^^

Here is the world without a flux capacitor at your side.::

    from datetime import datetime
    from pytz import timezone

    EST = "US/Eastern"
    UTC = "UTC"

    d = datetime.utcnow()
    utc = timezone(UTC)
    est = timezone(EST)
    d = utc.localize(d)
    d = est.normalize(EST)
    return d

Now lets warm up the `delorean`::

    from delorean import Delorean

    EST = "US/Eastern"

    d = Delorean(timezone=EST)
    return d

Look at you looking all fly. This was just a test drive checkout out what else
`delorean` can help with below.

Guide
=====

.. toctree::
    :maxdepth: 2

    license
    install
    quickstart
    interface
    contribution
    philosophy

