# Nevermore-Klipper

This is a simple include for the Nevermore. To use it with your printer, edit
the pin definition in line 16 so it matches your printer, then add a line 
[include nevermore.cfg] to your printer.cfg.

What you get:
- a generic fan "Nevermore" which is adjustable in GCODE and in Mainsail/Fluidd
- Commands in your 12864-controller to turn the fan on/off or adjust in 10%-steps
- a Macro to turn the fan off some time after the print.

Slicer integration: Add "SET_FAN_SPEED FAN=Nevermore SPEED=1" in your start-macro
(or less fan depending on your needs, like SPEED=0.8)
in your end print code, add "UPDATE_DELAYED_GCODE ID=filter_off DURATION=180"
this keeps your Nevermore running for 180s after the print finishes to clean the 
chamber a bit more.
