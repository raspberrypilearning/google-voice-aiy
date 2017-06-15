## Making your own actions

- An action is the thing that you want your voice kit to do. Below is about the most basic action you can come up with.

```python
class PrintHelloWorld():
	"""Prints Hello World!"""

	def run(self, voice_command):
	    print("Hello World!")
```

- All this will do is print `Hello World!` to the console when you run the program. If you add the following voice command in, you can test this out.

```python
    actor.add_keyword("hello world", PrintHelloWorld())
```

- Have a play around with this an see what else you can get the voice kit to do.
