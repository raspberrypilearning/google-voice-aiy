## Simple voice responses

The AIY Voice kit software allows you to add your own simple voice commands that will provide simple responses.

- Using a text editor or IDLE, open the file called `action.py`. You can find it at `/home/pi/voice-recognizer-raspi/src/action.py`.

- Most of this file contains instructions on how to use it, but if you scroll down, you will eventuall come to the following comments:
  
	``` python
	# =========================================
	# Makers! Add your own voice commands here.
	# =========================================
	```

- Here's where you can add some simple voice commands and the response you would like receive back. Underneath the comment, you can now add your own action. Try adding the following lines and make sure that you keep the indentation.

	``` python
	# =========================================
	# Makers! Add your own voice commands here.
	# =========================================
	
	actor.add_keyword("what's up", SpeakAction(say, "I'm fine, thank you"))
	```

- So what does this line do? `actor.add_keyword("what's up"` instructs the code to listen out for the keywords **"what's up"** to be spoken by the user. `SpeakAction(say, "I'm fine, thank you")`, instructs the program to respond with the words `"I'm fine, thank you"`

- Have a go at running this code, and test that it's working.

- Now try adding your own set of keywords and responses underneath the one you have just written.
