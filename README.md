# HOME_WORK_7_Rand
//Заполнить массив случайными числами. Генератор уникальных случайных чисел.
#include <iostream>
#include <ctime>
using namespace std;
int main()
{
	srand(time(NULL));
	const int SIZE = 10;
	int arr[SIZE];
	for (int i = 0; i < SIZE; i++)
	{
		arr[i] = rand() % 20;
		for (int j = 0; j < i; j++)
		{
			if (arr[i] == arr[j]) // Если i == j то i уменьшается на 1
			{
				i--;
				continue;
			}
		}
	}
	for (int i = 0; i < SIZE; i++)
	{
		cout << arr[i]<<" "; // вывод всех элементов массива в строку через пробел
	}
}
