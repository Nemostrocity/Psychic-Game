Aloha—This is the ReadMe for the Psychic Game,

The instructions are to:

The app randomly picks a letter, the user has to guess which letter the app chose. 
//Check

Put the following text on your page:

	Guess what letter I'm thinking of 
  //Slightly modified, check.

	Wins: (# of times the user has guessed the letter correctly) 
  //check

		When the player wins, increase the Wins counter and start the game over again (without refreshing the page). 
    //check

	Losses: (# of times the user has failed to guess the letter correctly after exhausting all guesses) 
  //check

		When the player loses, increase the Losses counter and restart the game without a page refresh (just like when the user wins).
    //check

	Guesses Left: (# of guesses left. This will update) 
  //check

	Your Guesses So Far: (the specific letters that the user typed. Display these until the user either wins or loses.) 
  //check I would have liked to have the program check to make sure only letters were guessed and that it would ignore repeated guesses of the same letter...

HTML for communicating to user //check

	
computer picks letter

user enters key

is key is = to computer letter
  ALERT USER WINS
    WIN++

  ELSE
  USER GUESS ADDED TO LIST
  GUES COUNT ++
  GUESSES LEFT --

  IS NUM GUESSES <1
   USER LOOSE++
    RESET GAME (CLEAR VARIABLE USERGUESS)






 