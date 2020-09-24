//This program will find the largest value in a 2d array


#include <iostream>
using namespace std;

void displayResults(int);

int main()
{
	//Variables
	const int NUM_ROWS = 3, NUM_COLUMNS = 4;
	int numArray[NUM_ROWS][NUM_COLUMNS] = { {18, 10, -7, 0}
						{-4, 13, 41, 60},
						{5, -19, 60, 4} },
		largestValue;

	//Process
	__asm
	{
		mov ecx, 12			//Set loop counter to size of array
		lea esi, numArray		//Move address of numArray to esi
		mov ebx, 0			//Move 0 to eax for index
		mov eax, [esi + ebx]		//Set eax to first array element
		loopHead:			//loopHead
			cmp [esi + ebx], eax	//Is the current array element greater than eax?
			jl noNewKing		//Yes, skip king assignment
			mov eax, [esi + ebx]	//No, assign new king to eax
			noNewKing:		//Place to continue loop processing
				add ebx, 4	//Increment array to next element
				loop loopHead	//Continue loop
		mov largestValue, eax		//Assign eax value to largestValue
	}

	//Display results
	displayResults(largestValue);

	//El done
	return 0;
}

/* ------------------------------------------------------------
 displayResults
 Displays the results of the program
 Receives: An int of the largest value in the array
 Returns: Nothing
 Requires: Nothing
 ------------------------------------------------------------ */
void displayResults(int largestValue)
{
	cout << "Largest value = " << largestValue;
}
