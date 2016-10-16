#include <iostream>
#include <string>

using namespace std;

struct DVD
{
	int id;
	string title;
	string rating;
	double price;
	string borrower;
};

//initializer list for an array
const int MAX = 5;
DVD DVDlist[MAX] = { {1, "John Wick", "rating", 29.99, }, {2, "Title", "rating", 29.99, },
	{ 3, "Title", "rating", 29.99, }, { 4, "Title", "rating", 29.99, }, { 5, "Title", "rating", 29.99, } };

//menu
//DisplayAllDvds
void DisplayAllDvds();
//DisplayDvdDetail
void DisplayDvdDetail();
//CheckOutDvd
void CheckOutDvd();
//CheckInDvd
void CheckInDvd();

int main()
{
	DisplayDvdDetail();

	system("pause");
	return 0;
}

//menu
//void Menu()
//{
//	cout <<
//}

//DisplayAllDvds
void DisplayAllDvds()
{
	
	//print out array using for loop
	for (int i = 0; i < MAX; i++)
	{
		int j = i;
		cout << ++j << " - " << DVDlist[i].title << endl;
	}
}

//DisplayDvdDetail
void DisplayDvdDetail() 
{
	int id = 0;

	cout << "Please enter DVD ID for display: ";
	cin >> id;
	id--;

	cout << "Title: " << DVDlist[id].title << endl;
	cout << "Rating: " << DVDlist[id].rating << endl;
	cout << "Price: $" << DVDlist[id].price << endl;
	cout << "Borrower: " << DVDlist[id].borrower << endl;

	//switch case to display dvds
}

//CheckOutDvd
//pass in struct? return struct? at least for borrower
void CheckOutDvd() 
{
	int id = 0;
	string name = "";

	cout << "Please enter DVD ID to checkout: ";
	cin >> id;
	//check to see if it is already checked out

	cout << "Please enter your name for checkout: ";
	//need to use get function for string?
	getline(cin, name);

	//return int for checkout identifier?
}

//CheckInDvd
//pass in struct? return struct? at least for borrower
void CheckInDvd() 
{
	int id = 0;

	cout << "Please enter the DVD ID for check in: ";
	cin >> id;
	//check if video is checked out

	//clear out borrower variable
}
