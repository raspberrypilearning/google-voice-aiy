## Using `voice_command`

Now that you can turn the LED on with a voice command, it would be nice if you could get it to stay on until another voice command turns it off again.

If you have a look at the `run` method you created, you should be able to see that it has a `voice_command` parameter.

```python
def run(self, voice_command):
	self.say("Turning on LED")
	led.on()
	sleep(5)
	self.say("Turning off LED")
	led.off()
```

This `voice_command` that is automatically passed to your `run` method is a string translation of whatever the Google Assistant API thinks you said. (It makes mistakes sometimes.)

Here's what you're going to do:

- Within your run method, convert the `voice_command` string into all lower case
- Search through the string.
    - If it contains the word "on", turn the LED on
    - If it contains the word "off", turn the LED off

- You can have a look at the section below to learn how to find a specific sequence of characters within a string using Python.

[[[generic-python-finding-substrings]]]

Don't worry if you're completely stuck - the hints below can help you out.

--- hints --- --- hint ---
- Your trigger should remain the same: it should be the "LED" keyword.
- Within the `run` method, create a new variable called `command` that is equal to the `voice_command`, but converted to lower case.
- If the string `on` is in the `command` string, then the LED can turn on.
- If the string `off` is in the `command` string, then turn the LED off.
--- /hint --- --- hint ---
Here's a bit of code to get you started:
``` pyton
def run(self, voice_command):
	command = ## make it all lower case
	if "on" in command:
		self.say('Turning LED on')
		## turn on the LED

	elif #something here :
		self.say('Turning LED off')
		## turn off the LED
```
--- /hint --- --- hint ---
Here's a little video showing you how to write the code:
<iframe width="560" height="315" src="https://www.youtube.com/embed/9qVe9gjCSKE" frameborder="0" allowfullscreen></iframe>
--- /hint --- --- /hints ---
