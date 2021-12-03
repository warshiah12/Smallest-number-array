# Smallest-number-array
#will display the smallest number out of 10 numbers
#include<iostream>
#include<array>
#include<algorithm>
#include<random>
using namespace std;
int main()
{
	int min, array[10];
	cout << "Enter 10 integer values: " << endl;

	for (int k = 0; k < 10; k++)
	{
		cout << "Number " << k + 1 << " : ";
		cin >> array[k];
		while (cin.fail() || array[k] < 0 || array[k] > 100)
		{
			cout << "\n\aThe number entered is not within the range of 1-100! " << endl;
			cout << "Enter the number again : ";
			cin.clear();
			cin.ignore();
			cin >> array[k];
		}
	}
	for (int k = 0; k < 10; k++)
	{
		if (array[0] > array[k])
			array[0] = array[k];
	}
	cout << "\nThe smallest number is: " << array[0];
	return 0;
}
