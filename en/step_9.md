## Making your own actions

Now it's time to make your own actions. As well as responding to particular commands, you can make the Raspberry Pi perform any action you like, when it receives a command.

- Scroll up to the section with the following comment:

```python
# =========================================
# Makers! Implement your own actions here.
# =========================================
```

- Beneath this you can add your own actions. Don't worry if you've never written a class before, as it can be ketp fairly simple.

- An action is the thing that you want your voice kit to do. Below is about the most basic action you can come up with.

	```python
	class PrintHelloWorld():

		def run(self, voice_command):
			print("Hello World!")
	```

- All this will do is print `Hello World!` to the console when you run the program, and the `run` method is called. To get this to happen you need to add another voice command. Scroll back down to where you added the previous voice command and add this in:

	```python
	actor.add_keyword("hello world", PrintHelloWorld())
	```

- Now run the program in the teminal again (`src/main.py`) and push the button on the Voice Kit. If you now say **Hello World**, you should see the output in the console.

