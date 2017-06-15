## Simple voice responses

The AIY Voice kit software allows you to add your own simple voice commands that will provide simple responses.

- Using a text editor or IDLE, open the file called `action.py`. You can find it at `/home/pi/voice-recognizer-raspi/action.py`.

- Most of this file contains instructions on how to use it, but if you scroll past the first set of comments, you should see the following code:

``` python
class SpeakAction(object):

    """Says the given text via TTS."""

    def __init__(self, say, words):
        self.say = say
        self.words = words

    def run(self, voice_command):
        self.say(self.words)
```
- This `class` does a few simple things. Don't worry if you're not too familiar with classes, as understanding what it does is more important.
  - The class starts by initialising (`__init__`) an object with two things. `self.say` is a special function defined in another file. This function handles all the complicated conversion of text to speech.
    - The class also initialises an object with `self.words`. This is again a sting, and represents what you want the Voice Kit to respond through the speaker. If `self.words` was the string `"I'm fine, thank you"`, then that is what the Voice Kit would respond.
  - The class has a `run` method. This has a `voice_command` parameter. The `voice_command` are all the words that you speak into the microphone.
  - In the run function are the actions that you need to be performed. In this case the `self.say(self.words` will just convert a string to speech for output through the speaker.
  
- To use this class, scroll down the code and have a look at the section where it says the following:

``` python
    # =========================================
    # Makers! Add your own voice commands here.
    # =========================================
```

- Here's where you can add some simple voice commands and their associated responses. Underneath the comment, you can now add your own action. Try adding the following lines and make sure that you keep the indentation.

``` python
    # =========================================
    # Makers! Add your own voice commands here.
    # =========================================
	actor.add_keyword(_("what's up"), SpeakAction(say, "I'm fine, thank you"))
```

- So what does this line do? `actor.add_keyword(_("what's up")` instructs the code to listen out for the keywords *"what's up"* to be spoken. When the keywords are recognised then the code within the `SpeakAction` class is run. What is passed in is the command the user spoke (`say`) and the string `"I'm fine, thank you"`. The `SpeakAction` code that you looked at earlier then outputs that string through the microphone.

- Have a go at running this code, and test that it's working.

- Now try adding your own set of keywords and responses underneath the one you have just written.
