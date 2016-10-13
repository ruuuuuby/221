# 221
#include "stdafx.h"
#include <iostream>
#include <fstream>
using namespace std;

bool isPrime(int);
void output();
ofstream outputfile;

int main()
{
	//ask the user to enter the number//
	int number;
	cout << "Please enter an integer\n";
	cin >> number;
	//go to the isPrime function and detect whether it is a prime and display//
	if (isPrime(number))
		cout << number << " is a prime\n";
	else
		cout << number << " is not a prime\n";
	//go to another function to display all primes from 1-100//
	output();
	return 0;
	}
bool isPrime(int number)
{
	//use bool to detect true or false//
	bool status;
	int a;
	//use a loop to make number divide all integers from 1 to itself//
	//if all integers can be divided with remain, the number is a prime//
	//make sure 1 and 2 is exception//
	if (number == 1 || number == 2)
	{
		status = true;
		return status;
	}
	for (a = 2;a < number;a++)
	{
		if (number%a == 0)
		{
			status = false;
			return status;
			break;
		}
	}
	
	if (number = a + 1)
		{
			status = true;
			return status;
		}	
}

void output()
{
	int b = 3;
	int c;
	ofstream outputfile;
	outputfile.open("prime2.txt");
	outputfile << "1\n2\n";
	while (b <= 100)
	{
		for (c = 2;c < b;c++)
		{
			if (b%c == 0)
			{
				break;
			}
		}
		outputfile << b << endl;
		b++;
	}
	outputfile.close();
}

 
    
