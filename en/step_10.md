## Controlling an LED

Now is your chance to try and make an LED turn on and off again when an command is given. Alter the code so that when the command "LED" is spoken, the LED turns on, stays on for 5 seconds, then switches off.

--- hints --- --- hint ---
1. Wire up an LED and a resistor to the header pins you soldered on.
2. Somewhere near the top of the file, you will need to import the `LED` class from the `gpiozero` module. You'll also want the `sleep` function from the `time` module.
3. You will want to create an `led` object on pin 17.
4. When the command to turn on the led is given, the `led.on()` method should be called, there should be a pause for a few seconds, then the `led.off()` method should be called.
--- /hint --- --- hint ---
![circuit](images/led-circuit.jpg)
--- /hint --- --- hint ---
<iframe width="560" height="315" src="https://www.youtube.com/embed/fnWZlFZHIJY" frameborder="0" allowfullscreen></iframe>
--- /hint ---
--- /hints ---
