# Advanced JavaScript: Constructor Word Guess

### Overview

In this application I have created you will create a Word Guess command-line game using node.js and constructor functions.

## To install the npm packages run these commands one at a time.

* npm install inquirer
* npm install random-words
* npm install node

## Commands to run LIRI
Follow the format presented in these queries

- node index.js 
- you will be prompted to enter your guesses
- the screen will show you how many letter are in the word
- the screen will show you your correct guesses
- you will be given 7 guesses
- your guesses will be printed back to you
- you will lose / decrement the guesses remaining by one everytime you guess incorrectly
- if you run out of guess the screen will diplay "YOU LOSE!"
- if you guess the word correctly the screen will display "YOU WIN"


## You can find an image of the output at the following link:

![Image of the start of the game output](https://github.com/jhwillia7/Word-Guess-Constructor-Style/images/Game-Start.PNG)

![Image of guesses output](https://github.com/jhwillia7/Word-Guess-Constructor-Style/images/Guesses.PNG)

![Image of YOU WIN output](https://github.com/jhwillia7/Word-Guess-Constructor-Style/images/You-Win.PNG)

![Image of YOU LOSE! output](https://github.com/jhwillia7/Word-Guess-Constructor-Style/images/You-Lose.PNG)

* **About the Game**: 

## letters.js
Contains a constructor, Letter. This constructor displays an underlying character or a blank placeholder (an underscore), depending on whether or not the you have guessed the letter. That means the constructor defines:

  * A string value to store the underlying character for the letter

  * A boolean value that stores whether that letter has been guessed yet

  * A function that returns the underlying character if the letter has been guessed, or a placeholder (like an underscore) if the letter has not been guessed

  * A function that takes a character as an argument and checks it against the underlying character, updating the stored boolean value to true if it was guessed correctly

## word.js
Contains a constructor, word that depends on the Letter constructor. This is used to create an object representing the current word the user is attempting to guess. That means the constructor defines:

  * An array of `new` Letter objects representing the letters of the underlying word

  * A function that returns a string representing the word. This calls the function on each letter object (the first function defined in `letter.js`) that displays the character or an underscore and concatenates those together.

  * A function that takes a character as an argument and calls the guess function on each letter object (the second function defined in `Letter.js`)

## index.js
The file containing the logic for the course of the game, which depends on `word.js` and:

  * Randomly selects a word and uses the `word` constructor to store it

  * Prompts the user for each guess and keeps track of the user's remaining guesses

3. `letter.js` *does not* `require` any other files.

4. `word.js` *does only* require `letter.js`
