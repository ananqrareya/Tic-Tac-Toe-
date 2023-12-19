# Tic-Tac-Toe- game written in Dart .
 Here's how to run it:
 
 *Environment Setup:
- Make sure you have Dart installed on your system. You can download it from https://dart.dev/get-dart.
- Open a terminal in your project directory (where the Dart files are located).

* Running the Game:
- Run the following command in the terminal: dart run tic_tac_toe.dart.

*Gameplay:
- Once the game starts, you will be prompted to choose your marker (X or O).
- Then, your turn will begin. Enter a number between 1 and 9 to mark your position on the board.
- The game will display the updated board and check for win conditions after each turn.
- If you win, the game will declare you the winner and show the final board.
- If the board fills up without a winner, it will be a draw.
- After each game, you will be asked if you want to play again.

*Code Structure:
- The main functions are stored in the tic_tac_toe.dart file.
- Key functions include:
- playGame: Manages the overall game loop, including turn taking and win conditions.
- printboard: Displays the current state of the board.
- choiceOfPlayers: Lets players choose their markers.
- boardlocations: Checks if the chosen position is within the board range.
- boardPosition: Checks if the chosen position is empty.
- win: Determines if a player has won based on the current board state.
- boardisFull: Checks if the board is full.
- playAgain: Asks players if they want to restart the game.

*Customization:
- This is a basic Tic-Tac-Toe game. You can customize it further by adding features like:
- Difficulty levels for the AI opponent.
- Multiplayer mode for playing against other players.
- Different board sizes (e.g., 4x4 or 5x5).

  I hope this README helps you run and enjoy this Tic-Tac-Toe game!
