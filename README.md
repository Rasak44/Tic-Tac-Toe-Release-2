# Tic-Tac-Toe-Release-2

/*
* Name: Test.c
* Program to create a basic Tic-Tac-Toe
* Start Date: 03/26/2022
* Author: Mark Plucinski
*/



#include "stdio.h"

#define ROW 3
#define COL 3


/*
int board[25] = {
	:,:,:,:,:,
	:,O,-,X,:,
	:,X,-,-,:,
	:,-,-,-,:,
	:,:,:,:,:,	
}
	*/
// Create the constants for the board pieces
const NOUGHTS = 1;
const CROSSES = 2;
const BORDER = 8;
const EMPTY = 0;

const int ConvertTo25[9] = {
	6,7,8,
	11,12,13,
	16,17,18
};
//Base board design
void InitialiseBoard(int *board) {
	int index = 0;

	for (index = 0; index < 25; ++index) {
		board[index] = BORDER;
	}

	for (index = 0; index < 9; ++index) {
		board[ConvertTo25[index]] = EMPTY;
	}
}
//Initial welcome information and the board print design
void PrintBoard(const int* board) {
	int index = 0;
	printf("\nWelcome to my Tic-Tac-Toe Game\nBy: Mark Plucinski\n\n\nBoard:\n");
	for (index = 0; index < 25; ++index) {
		if(index !=0 && index%5==0) {
			printf("\n");
		}
		printf("%4d", board[index]);
	}

{
int *ptr1, *ptr2;

ptr1 = NOUGHTS;
ptr2 = CROSSES;

}

//Contains the area where you can add "board[ConvertTo25[0]] =" with the addition of "CROSSES;" or "Nought;" for X or O
int main();
{
	int board[25];
	InitialiseBoard(&board[0]);
	board[ConvertTo25[0]] = CROSSES;
	board[ConvertTo25[3]] = NOUGHTS;
	board[ConvertTo25[5]] = CROSSES;
	PrintBoard(&board[0]);

	return 0;
}

// constants
const char s[3] = { '*', 'X', 'O' };

int getWinnder(int board[3][3]);
{
	int win = 0;

// checks for three same value horizontal
	for (int i = 0; i < 3; i++)
		if (board[i][0] == board[1][i] && board[i][1] == board[i][2])
			win = board[i][0];

//Checks for three same value vertical
	for (int i = 0; i < 3; i++)
		if (board[0][i] == board[1][i] && board[1][i] == board[2][i])

			//Checks for three same value diagnal
			if (board[0][0] == board[1][1] && board == board[2][2])
				(board[0][2] == board[1][1] && board[1][1] == board[2][0]);

return win;
}
