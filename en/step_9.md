## Making your own actions

Now it's time to make your own actions. As well as responding to particular commands, you can make the Raspberry Pi perform any action you like when it receives a specific command.

- Scroll up to the section with the following comment:

```python
# =========================================
# Makers! Implement your own actions here.
# =========================================
```

- Below this you can add your own **actions**. An action is the thing that you want your Voice Kit to do. Below is about the most basic action you can come up with. Don't worry if you've never written a **class** before, as it can be kept fairly simple.

	```python
	# =========================================
	# Makers! Implement your own actions here.
	# =========================================
	
	class PrintHelloWorld():

		def run(self, voice_command):
			print("Hello World!")
	```
- Within the class `PrintHelloWorld()` is a single function called `run()`. Functions inside classes are called **methods**. This method will be automatically used by the Voice Kit software.

- All this class will do is print `Hello World!` to the console when the `run` method is called. To make this happen, you need to add another voice command. Scroll back down to where you added the previous voice command and add in another `keyword`.

	```python
	# =========================================
	# Makers! Add your own voice commands here.
	# =========================================
	
	actor.add_keyword("what's up", SpeakAction(say, "I'm fine, thank you"))
	actor.add_keyword("hello world", PrintHelloWorld())
	```

- Now run the program in the teminal again (`src/main.py`) and push the button on the Voice Kit. If you now say "Hello world!", you should see the output in the console.

