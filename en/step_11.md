## Getting some feedback

It would be nice if you could get the class you have written to give some verbal feedback when the LED switches on and off again. To do this you will need to use that `say` function that was discussed earlier.

To use the `say` function it needs to be included in the `actor.keyword` call. It can then be used in the class when you initialise the class.

- First you can alter your command section of the script. The `ControlLED` needs to use the `say` function and to be passed a string.

	``` python
	actor.add_keyword('LED', ControlLED(say))
	```

- Now that you're using some parameters with your `ControlLED` class, you need to make sure you can use them in the class' methods. You do this in the initialisation method.

	```python
	class ControlLED():
		"""Turns on an LED for 5 seconds"""

		def __init__(self, say):
			self.say = say
		```

- Now within your `run` method you can call `self.say` and pass it the string you want the Voice Kit to say..

	``` python
	def run(self, voice_command):
		self.say("Turning on LED")
		led.on()
		sleep(5)
		led.off()
	```
