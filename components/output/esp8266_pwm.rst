ESP8266 Software PWM Output
===========================

.. seo::
    :description: Instructions for setting up ESP8266 software-based PWMs.
    :image: pwm.png

The ESP8266 Software PWM platform allows you to use a software PWM on
the pins GPIO0-GPIO16 on your ESP8266. As this is only a software PWM
and not a hardware PWM (like the :doc:`ESP32 LEDC PWM <ledc>`) and has a key
disadvantage: There can be a noticeable amount of flickering with increased WiFi
activity.

If you need a stable PWM signal, it’s definitely recommended to use the
successor of the ESP8266, the ESP32, and its :doc:`ESP32 LEDC PWM <ledc>` instead.

.. code-block:: yaml

    # Example configuration entry
    output:
      - platform: esp8266_pwm
        pin: D1
        frequency: 1000 Hz
        id: pwm_output

Configuration variables:
------------------------

- **pin** (**Required**, :ref:`Pin Schema <config-pin_schema>`): The pin to use PWM on.
- **id** (**Required**, :ref:`config-id`): The id to use for this output component.
- **frequency** (*Optional*, frequency): The frequency to run the PWM with. Lower frequencies
  have more visual artifacts, but can represent much more colors. Defaults to ``1000 Hz``.
- All other options from :ref:`Output <config-output>`.

See Also
--------

- :doc:`/components/output/index`
- :doc:`/components/output/ledc`
- :doc:`/components/light/monochromatic`
- :doc:`/components/fan/speed`
- :doc:`/components/power_supply`
- :apiref:`output/esp8266_pwm_output.h`
- :ghedit:`Edit`

.. disqus::
