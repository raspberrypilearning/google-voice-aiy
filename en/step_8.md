## Simple voice responses

The AIY Voice Kit software allows you to add your own simple voice commands that will result in simple responses.

- Using a text editor or IDLE (**Menu** --> **Programming** --> **Python 3 (IDLE)**, open the file called `action.py`. You can find it in `/home/pi/voice-recognizer-raspi/src/action.py`.

- Most of this file consists of instructions on how to use the kit, but if you scroll down, you will eventually come to the following comments:
  
	``` python
	# =========================================
	# Makers! Add your own voice commands here.
	# =========================================
	```

- Here's where you can add some simple voice commands and the response you would like to receive back. Below the comment, you can now add your own actions. Try adding the following lines - make sure that you keep the indentation.

	``` python
	# =========================================
	# Makers! Add your own voice commands here.
	# =========================================
	
	actor.add_keyword("what's up", SpeakAction(say, "I'm fine, thank you"))
	```

- What does this line do? `actor.add_keyword("what's up"` instructs the code to listen for the keywords **"what's up"** spoken by the user. `SpeakAction(say, "I'm fine, thank you")`, instructs the program to respond with the words `"I'm fine, thank you"`.

- Have a go at running this code, and test that it's working. You'll need to go back to the terminal window, press `Ctrl + C` if the progam is currently running, and then type `src/main.py` to restart the Voice Kit software.

- Push the button and then ask the Voice Kit "What's up?"

- Now try adding your own set of keywords and responses below the one you have just written.
