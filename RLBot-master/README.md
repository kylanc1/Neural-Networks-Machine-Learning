RLBot:

Short Description:
RLBot is a framework to create bots to play rocket league that reads values from the game and outputs button presses to the game.  RLBot works for 1v1 exhibition games of player vs player opponent.  I use vjoy + pyvjoy + x360ce to acheive the controller simulation.  All autonomous bots that are created should be fed game values as input and perform whatever processing they wish before outputting key presses as output. The idea is to allow player made bots to be interchangeable.  One of the bots being worked on, and my initial project, requires Google Tensorflow.

Requirements:
Windows, Rocket League, vjoy + pyvjoy + x360ce at least.  If you are running the tensorflow bot than definitley need (Python 3.5, Google Tensorflow).

Reading Values From Game:
RLBot is fed values from an injected dll.  These values include amount of boost, xyz positional coordinates for player, ball, and opponent, rotational values, and score from the game to name a few.  Look at cStructure.py for an idea of all values.  I use CheatEngine to inject the dll for now.

Runner:
Inject the dll into RocketLeague first (only need to do this step once each time you open rocketleague) Run "python runner.py" after the game is loaded and all bots and the ball are loaded on the playfield.  A GUI window should pop up after a second displaying game values.

p2join scripts:
In order to get player 2 to join in you need to press start initially, you also need to press a at the team selection menu.  I have a couple scripts that just wait a couple seconds and then press and release the button for this purpose.  So to run them you can just minimize out rocket league, start the script, and pop back into the game and it'll press the button for you.