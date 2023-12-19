 import 'dart:core';
import 'dart:io';

const String playerX = 'X';
const String playerO = 'O';
List<String> board = [' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' '];
String currentPlayer = playerX;
void main() {
  playGame(); //Start Playing :
  playAgain();
}

/*
Function : playGame():
A function to show the player what he can enter on the board
 and show him the results and also inform him if he wins or not .
 */
void playGame() {
  choiceOfPlayers(); //Decide which player you will be
  while (true) {
    printboard();
    print("It is Player " +
        currentPlayer +
        " Enter your place on the board within the range (1-9)");
    int place;
    String input = stdin.readLineSync()!;
    place = int.parse(input);
    if (!boardlocations(place) && !boardPosition(place)) {
      print('Invalid input. Please enter a number between 1 and 9.');
      continue;
    }
    if (!boardPosition(place)) {
      print('not correspond to an empty cell on the board.');
      continue;
    }
    board[place - 1] = currentPlayer;
    if (win(currentPlayer)) {
      print("Player : $currentPlayer wins!");
      printboard();
      print("\n");
      break;
    } else if (boardisFull()) {
      print("It's A Draw!");
      print("\n");
      printboard();
      break;
    } else
      currentPlayer = currentPlayer == playerX ? playerO : playerX;
  }
}

/*
Function printboard():
Players are shown the game board in each case.
 */
void printboard() {
  for (int i = 0; i < 9; i += 3) {
    print("${board[i]} | ${board[i + 1]} | ${board[i + 2]}");
  }
  print("\n");
}

/*
Function choiceOfPlayers():
Provides the choose for the  to select the player symbol X or O :
 */
void choiceOfPlayers() {
  print('Player 1 :  choose your marker (X or O):"\n');
  String choose = stdin.readLineSync()!.toUpperCase();
  while (choose.toUpperCase() != "X" && choose.toUpperCase() != "O") {
    print("Invalid choice. Please choose X or O: ");
    choose = stdin.readLineSync()!.toUpperCase();
  }
  currentPlayer = choose;
  print("Player 2, your marker is " + (currentPlayer == "X" ? "O" : "X"));
}

/*
Function boardlocations():
Checking  if the player chooses  place he is in among the board positions or not .
 */
bool boardlocations(int place) {
  if (place < 1 || place > 9) {
    return false;
  }
  return true;
}

/*
Function : boardPosition():
Checking whether the player has chosen the non-reserved place on the board.
 */
bool boardPosition(int place) {
  if (board[place - 1] != " ") {
    return false;
  }
  return true;
}

/*
Function win() :
To determine the results of the game and whether one of the players met the winning conditions or not.
 */
bool win(String player) {
  //Checking rows
  if (board[0] == board[1] && board[0] == board[2] && board[0] != " ") {
    return true;
  }
  if (board[3] == board[4] && board[3] == board[5] && board[3] != " ")
    return true;

  if (board[6] == board[7] && board[6] == board[8] && board[6] != " ") {
    return true;
  }
  //Checking columns
  if (board[0] == board[3] && board[0] == board[6] && board[0] != " ") {
    return true;
  }
  if (board[1] == board[4] && board[1] == board[7] && board[1] != " ") {
    return true;
  }
  if (board[2] == board[5] && board[2] == board[8] && board[2] != " ") {
    return true;
  }

  // Checking Diagonal
  if (board[0] == board[4] && board[0] == board[8] && board[0] != " ") {
    return true;
  }
  if (board[2] == board[4] && board[2] == board[6] && board[2] != " ") {
    return true;
  }
  return false;
}

/*
Function boardisFull() :
Check whether the game board is full or not.
 */
bool boardisFull() {
  return !board.contains(" ");
}

/*
Function : playAgain() :
After the end of each competition, we are given the option to restart the game.
 */
void playAgain() {
  print("Do you want to Play Again? (yes/no)");
  String answer = stdin.readLineSync()!.toLowerCase();
  if (answer.toLowerCase() == "yes") {
    board.clear();
    board.addAll(List.filled(9, " "));
    currentPlayer = playerX;
    main();
  } else {
    print("Thanks for playing!");
    return;
  }
}

