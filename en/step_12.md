## Using `voice_command`

Now that you can turn the LED on with a voice command, it would be nice if you could get it to stay on, until another voice command turns it off again. The argument `voice_command` that is passed to your `run` method is whatever the users says, as a string.

Here's the basic logic that you will need to follow.

- Take the `voice_command` string.
- If the `voice_command` contains the word **on**:
    - turn on the LED
- If the `voice_command` contains the word **off**
    -  turn the LED off.

You can have a look at the section below, to learn how to find a specific sequence of characters within a string using python, if you need help.

[[[generic-python-finding-substrings]]]

Don't worry if you're completely stuck - the hints below can help you out.

--- hints --- --- hint ---
- Your trigger should remain the same - listening for the LED key word.
- Within the `run` method can use the `voice_command`.
- If the `voice_command` contains the string `on` then the LED can turn on.
- If the voice command contains the string `off` then the LED turns off
--- /hint --- --- hint ---
Here's a little code to get you started:
``` pyton
def run(self, voice_command):
	command = ## make it all lower case
	if "on" in command:
		self.say('Turning LED on')
		## turn on the LED

	elif #something here :
		self.say('Turning LED off')
		## turn off the led
```
--- /hint --- --- hint ---
Here's a little video showing you how to write the code.
<iframe width="560" height="315" src="https://www.youtube.com/embed/9qVe9gjCSKE" frameborder="0" allowfullscreen></iframe>
--- /hint --- --- /hints ---
