# WSQ-3_PickANumber
This program is basically a game where the program itself chooses a random number between 1 and 100 and then asks the user to guess that number. The program will tell if the given number is lower or higher and will give you infinite tries until the user guesses the right number.
/*
PickANumber.cpp
Aug 21, 2017
Dulca
*/
#include <iostream>
#include <ctime>
#include <cstdlib>
using namespace std;
int main()
{
int Random, Num ,Guess;

srand(time(0)) ;
Random = (rand()%100+1) ;	//Generates a random number and saves it as Random
Guess = 0 ;

	cout << "I have a number between 1 and 100." << endl ;
	cout << "Please guess a number between them:" << endl ;

	while(Num != Random){	//While Num is different from Random...
		cin >> 	Num ;
		Guess = Guess + 1 ;
		if (Num != Random){	//If Num is different from Random do...
			if (Num < Random) {
				cout << "Oops, " << Num << " is too low, try again:" << endl ;
			} else {
				cout << "Oops, " << Num << " is too high, try again:" << endl ;
			}
		}
	}
	// If Num = Random then the program ends
	cout << "Congratulations! " << Num << " is the right answer." << endl ;
	cout << "You made " << Guess << " guesses to get the right answer." << endl ;
return 0;
}
