# Tic-Tac-Toe

Before we start coding I figured I’d give a quick summary of the game and talk about how I am going to approach coding it. First of all we are going to assume that X’s always go first, letting the user make the first move. We will get input from the console with a number 1-9. Where each number represents a different number in the grid (top left is 1, bottom right is 9). Once the user moves the computer will automatically decide on it’s move and make it. I am going to be using one main game loop that calls a few different functions. Each heading of this text based tutorial will likely tell you which function is being completed.

## Creating a Board
Like I mentioned above we will be using a grid system to represent our board. To do this in python we will create a list called board that will start off with 10 empty values. The reason we have 10 empty values rather than 9 is because when we get input from the user they can type numbers 1-9 NOT 0-8. So to make our lives easier we are going make the first value of our list an empty string. This way when we index elements in our list we can use 1-9 not 0-8.

## insertLetter()
This function is going to take two parameters: letter & pos. It is simply going to insert the given letter at the given position.

## spaceIsFree(pos)
This function will simply tell us if the given space is free. Meaning it does not already contain a letter. It has one parameter, pos, which will be an integer from 1-9.

## printBoard(board)
This function takes the board as a parameter and will display it to the console.

## isWinner()
This function will tell us if the given letter has won based on the current board. It has two parameters: bo(board) & le(letter). The letter must be a “X” or an “O”. We will simply check each possible winning line on the board and see if it is populated by the given letter.

## main()
This function is what we will call to start the game. It will be calling all of the different functions in our program and dictate the flow of the program.

## isBoardFull()
This function takes board as parameter and will simply return True if the board is full and False if it is not.

## playerMove()
In this function we will be asking the user to input a move and validating it. If the move is valid we will add that letter to the board. Otherwise we will continue to ask the user for input.

## compMove()
Now time for the AI! This function will be responsible for making the computers move. It will examine the board and determine which move is the best to make. The algorithm we will follow to do this is listed below.

If the current step cannot be completed proceed to the next.
1. If there is a winning move take it.
2. If the player has a possible winning move on their next turn move into that position.
3. Take any one of the corners. If more than one is available randomly decide.
4. Take the center position.
5. Take one of the edges. If more than one is available randomly decide.
6. If no move is possible the game is a tie.

## selectRandom()
This function will randomly decide on a move to take given a list of possible positions.

## Starting the Game
Now that we have all our functions completed all that’s left to do is start the game. If we just wanted to run the game once all we would have to do is call main. However, in our case we want the game to keep running until the user doesn’t want to play anymore, so we will create a small while loop in the main line.
