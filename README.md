# The Hangman Game

The `Game` class represents the game logic for a hangman game. It incorporates modules for display, serialization, and game options. The class provides methods for starting, playing, and managing the hangman game.

Upon initialization, the `Game` class selects a secret word from a dictionary file and sets up the game with the secret word, remaining letters, incorrect guesses, and a guess. The `start` method displays a start screen, prompts the player for an option (new game or load game), and proceeds accordingly.

The `select_secret_word` method randomly selects a word from a dictionary file, ensuring the word's length is between 5 and 12 characters. The `word_cracked?` method checks if the secret word has been fully guessed or if the player has guessed the entire word. The `game_is_over?` method determines if the game is over by checking if the player has made 7 incorrect guesses or if the secret word has been fully guessed. The `no_matches?` method checks if the current guess has no matches in the remaining letters.

The `update_display` method clears the screen and displays the hangman drawing, the status of the secret word, and the guess prompt. The `proceed_with` method handles the logic for loading a saved game or starting a new game based on the selected option. The `update_incorrect_guesses` method adds the current guess to the incorrect guesses if there are no matches. The `save` method prompts the player to save the game and performs the serialization to save the game state to a file.

The `correct_guesses` method retrieves the correct guesses made by the player so far. The `already_guesses?` method checks if a guess has already been made by the player. The `valid_guess` method retrieves a valid guess from the player, ensuring it is not already guessed and not empty.

The `run_game_loop`  method continues the game loop until the game is over. It updates the display, gets a valid guess from the player, and handles special in-game options such as saving the game. The `play` method starts the game loop, updates the display, displays the game over message, and prompts the player for an option to continue or exit.

This implementation of the hangman game provides an interactive and engaging experience for players. It allows players to start new games, load saved games, make guesses, save their progress, and play until the game is won or lost.
