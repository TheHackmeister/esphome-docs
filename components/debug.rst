Debug Component
===============

.. seo::
    :description: Instructions for setting up the debug component in esphomelib
    :image: bug-report.png

The ``debug`` component can be used to debug problems with esphomelib. At startup, it prints
a bunch of useful information like reset reason, free heap size, esphomelib version and so on.

.. figure:: images/debug.png
    :align: center

    Example debug component output.

.. code-block:: yaml

    # Example configuration entry
    debug:

    # Logger must be at least debug (default)
    logger:
      level: debug

There are no configuration variables for this component.

See Also
--------

- :doc:`logger`
- :apiref:`debug_component.h`
- :ghedit:`Edit`

.. disqus::
