#include <iostream>
#include <ctime>
using namespace std;
double random(double a, double b)
{
	return (double)(rand()) / RAND_MAX * (b - a) + a;
}
void input1_of_array(double *arr, int n)
{
	cout << "Please, enter the elements of the array: " << endl;
	for (int i = 0; i < n; i++)
	{
		cin >> *(arr + i);
	}
}
void input2_of_array(double *arr, int n)
{
	srand(time(NULL));
	cout << "What are the left and the right limits of the random numbers's range?" << endl;
	int a, b;
	cout << "Left limit = ";
	cin >> a;
	cout << "Right limit = ";
	cin >> b;
	cout << "Here is the filled in array by random values: " << endl;
	for (int i = 0; i < n; i++)
	{
		*(arr + i) = random(a, b);
		cout << *(arr + i) << " ";
	}
	cout << endl;
}
double search_of_max_elements(double *arr, int n)
{
	double max = *arr;
	for (int i = 1; i < n; i++)
	{
		if (arr[i] > max) max = arr[i];
	}
	return max;
}
double search_of_min_elements(double *arr, int n)
{
	double min = *arr;
	for (int i = 1; i < n; i++)
	{
		if (arr[i] < min) min = arr[i];
	}
	return min;
}
void output_of_changed_array(double *arr, int n, double max, double min)
{
	cout << "The changed array is:"<< endl ;
	for (int i = 0; i < n; i++)
	{
			if (arr[i] == max)
			{
				arr[i] = min;
			}
			else
			if (arr[i] == min)
			{
				arr[i] = max;
			}
			cout << arr[i] << " ";
	}
	cout << endl << endl;
}

int main()
{
	int n;
	cout << "Please, enter the number of the array's elements: ";
	cin >> n;
	double *arr = new double[n];
	cout << "Would you like to fill in the array with the help of keyboard or fill in the array by random elements?" << endl<<endl;
	cout << "Please, print 1 if you choose the first variant or 2 if you choose the second variant:" << endl;
	int variant;
	cin >> variant;
	cout << endl;
	switch (variant)
	{
		case 1:
		{
			input1_of_array(arr, n);
			break;
		}
		case 2:
		{
			input2_of_array(arr, n);
			break;
		}
	}
    double max = search_of_max_elements(arr, n);
	double min = search_of_min_elements(arr, n);
	cout << endl << "Min element = " << min << endl;
	cout <<"Max element = " << max << endl << endl;
	output_of_changed_array(arr, n, max, min);
	system("pause");
}
