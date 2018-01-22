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

HTML for communicating to user

	OPTION 1
	<body>
    <div class="container">
      <div class="row">
        <div class="col-md-offset-2 col-md-8">
          <div class="jumbotron">
            <h2>You just typed <span id="user-text"><strong>...Nothing.</strong></span></h2>
          </div>
        </div>
      </div>
    </div>

    <!-- We have to put this at the end of our document to ensure the user-text
         span exists when we try to access it. -->
    <script type="text/javascript">
      // Let's start by grabbing a reference to the <span> below.
      var userText = document.getElementById("user-text");

      // Next, we give JavaScript a function to execute when onkeyup event fires.
      document.onkeyup = function(event) {
        userText.textContent = event.key;
        console.log(event);
      };
    </script>
  </body>


  Option 2

  	  <body>
  <h1>Enter "h" to honk your horn, "d" to drive around the World, or "t" to get a tunne up...</h1>
  <div id="game">

  </div>
    <script>

      var car = {
        make: "Honda",
        model: "Fit",
        color: "Blue Raspberry",
        mileage: 3000,
        isWorking: true,

        driveToWork: function() {

          alert("Old Mileage: " + this.mileage);

          this.mileage = this.mileage + 8;

          alert("New mileage: " + this.mileage);
        },

        driveAroundWorld: function() {

          alert("Old Mileage: " + this.mileage);

          this.mileage = this.mileage + 24000;

          alert("New Mileage: " + this.mileage);
          alert("Car needs a tuneup!");

          this.isWorking = false;
        },

        getTuneUp: function() {
          alert("Car is ready to go!");
          this.isWorking = true;
        },

        honk: function() {
          alert("Honk! Honk!");
        }
      };


    // Whenever a key is pressed, alert "pressed a button".
    document.onkeyup = function(event) {
     
     var userGuess = event.key;

     if ((userGuess === "h") || (userGuess === "d") || (userGuess === "t")) {
      
          var html =
      "<p>You chose: " + userGuess + "</p>" +
   
       "<p></p>" +
          "<p>wins: " + wins + "</p>" +
          "<p>losses: " + losses + "</p>" +
          "<p>ties: " + ties + "</p>";      

        // Set the inner HTML contents of the #game div to our html string
        document.querySelector("#game").innerHTML = html;
        };

      // How would we log...

      // The car's make?
// console.log("Car's make:" + car.make);
//       // The car's model?
// console.log("Car's model:" + car.model);

//       // The car's mileage?
// console.log("Car's model:" + car.mileage);

//       // How would we run the car's driveToWork method?
// console.log("Milage after driven to work:" + car.driveToWork());

//       // How would we run the car's driveAroundWorld method?
// console.log("Milage after driving around the world(more or less):" + car.driveAroundWorld());

//       // How would we run the getTuneUp method?
// console.log("You're all set:" + car.getTuneUp() + car.honk());
    </script>
    
  </body>


Option 3

	  	<script type="text/javascript">
	var score = 0;
	var startingQuestion = 1;
	var numberQuesions = 10;
	var quiz = { 	 
  	 q1: ["Does San Francisco have a problem with homeless people?", "t"],
  	 q2: ["Is rent crazy expensive in San Francisco", "t",],
  	 q3: ["Does BART in SF resemble hell if lights were out?", "t"],
  	 q4: ["Would I move to any other city in the USA?", "f"],
  	 q5: ["Does San Francisco a whimsical architecture?","t"],
  	 q6: ["Is the climate one of the most preferable in the world?", "t"],
  	 q7: ["Are there good job opportunities in San Francisco?", "t"],
  	 q8: ["Are there good schools in San Francisco?", "t"],
  	 q9: ["Is there diverse cuisine in SF?", "t"],
  	 q10: ["Is San Francisco surrounded by incredible nature?", "t"]
};

function loadGame(){
	var questionHtml = "<p>SCORE: " + score + "</p>"
	document.querySelector("#scorePlace").innerHTML = questionHtml;
	 
	var answerHtml = quiz["q"+ startingQuestion][0]
	document.querySelector("#questionPlace").innerHTML = answerHtml;
}

loadGame()

document.onkeyup = function(event) {
	var userInput = event.key;
	if(userInput === "t" || userInput === "f"){
		checkAnswer(userInput)
	}
};
 
function checkAnswer(userInput){
	if(quiz["q"+ startingQuestion][1]===userInput){
		score = score + 1;

		incrementQuestion()
		reloadInfo()
	}else{
		incrementQuestion()
		reloadInfo()
	}
}
function reloadInfo(){
	var scoreHtml = "<p>SCORE: " + score + "</p>"
	document.querySelector("#scorePlace").innerHTML = scoreHtml;
	 
	var questionHtml = quiz["q"+ startingQuestion][0]
	document.querySelector("#questionPlace").innerHTML = questionHtml;
}
function incrementQuestion(){
	if(startingQuestion <= numberQuesions){
		startingQuestion = startingQuestion + 1;
	}
	else{

		var scoreHtml = "<h1>GAME OVER</h1>"
		document.querySelector("#scorePlace").innerHTML = scoreHtml;
		document.querySelector("#questionPlace").innerHTML = questionHtml;
	}
	
}

       
  	
  </script>
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
