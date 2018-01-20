Aloha—This is the ReadMe for the Psychic Game, which will be modified before shipping. 

For now this will serve as my psuedoCode Board

The instructions are to:

The app randomly picks a letter, the user has to guess which letter the app chose. 

Put the following text on your page:

	Guess what letter I'm thinking of

	Wins: (# of times the user has guessed the letter correctly)

		When the player wins, increase the Wins counter and start the game over again (without refreshing the page).

	Losses: (# of times the user has failed to guess the letter correctly after exhausting all guesses)

		When the player loses, increase the Losses counter and restart the game without a page refresh (just like when the user wins).

	Guesses Left: (# of guesses left. This will update)

	Your Guesses So Far: (the specific letters that the user typed. Display these until the user either wins or loses.)


Random number * 25 picks letter

upOnKey determine key clicked

if userKey = glyph 
	user wins
	else add key to userGuesses

	for var userTries = 8; userTries>0; userTries --; {

	}

	count attempts left
if at the end of the for loop no match, user looses...

show letters guessed by user

variants: images of the cards used in ghost busters
