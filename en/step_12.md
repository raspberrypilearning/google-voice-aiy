## Using `voice_command`

Now that you can turn the LED on with a voice command, it would be nice if you could get it to stay on, until another voice command turns it off again.

Here's the basic logic that you will need to follow.

- If the keyword LED is used, then use the ControlLED class
- If the `voice_command` contains the word **on** then turn the LED on
- If the `voice_command` contains the word **off** then turn the LED off.

You can have a look at the section below, to learn how to find a specific sequence of characters within a string using python, if you need help.

[[[generic-python-finding-substrings]]]

--- hints --- --- hint ---
- Your trigger should remain the same - listening for the LED key word.
- Within the `run` method can use the `voice_command`. If the `voice_command` contains the string `on` then the LED can tun on. If the voice command contains the string `off` then the LED turns off
--- /hint --- --- hint ---
Here's a little code to get you started:
``` pyton
    def run(self, voice_command):
		command = 
		if "on" in command:
			self.say('Turning LED on')
			
		elif #something here :
			self.say('Turning LED off')
```
--- /hint --- --- hint ---
Here's a little video showing you how to write the code.
<iframe width="560" height="315" src="https://www.youtube.com/embed/9qVe9gjCSKE" frameborder="0" allowfullscreen></iframe>
--- /hint --- --- /hints ---
