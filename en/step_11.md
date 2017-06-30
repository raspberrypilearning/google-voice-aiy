## Using the `say` function


It would be nice if you could get the class you have written to give some verbal feedback when the LED switches on and off again. To do this, you will need to use the special `say` function.

If you want to use the `say` function in your classes, it needs to be included in the `actor.keyword` call.

- First you can alter your voice command section of the script. The `ControlLED` class needs to use the `say` function.

	``` python
	actor.add_keyword('LED', ControlLED(say))
	```

- Since you want to use some parameters with your `ControlLED` class, you need to make sure you're allowed to use them by amending the class's methods. You do this in the initialisation method.

	```python
	class ControlLED():
		"""Turns on an LED for 5 seconds"""

		def __init__(self, say):
			self.say = say
	```

- Now within your `run` method, you can call `self.say` and pass it the string you want the Voice Kit to say.

	``` python
	class ControlLED():
		"""Turns on an LED for 5 seconds"""

		def __init__(self, say):
			self.say = say
			
		def run(self, voice_command):
			self.say("Turning on LED")
			led.on()
			sleep(5)
			self.say("Turning off LED")
			led.off()
	```
