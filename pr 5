#include <iostream>
#include <algorithm>

using namespace std;

int main() {
 setlocale(LC_ALL, "rus");
    int n;
    int key;
    cout << "Введите размер массива: "; 
    cin >> n;
    int* arr = new int[n];
    int a = 0;
    cout << "Введите способ заполнения массива 1-авто 2 - ручное: ";
    cin >> a;
    switch (a)
    {
        case 1:
        {
            for (int i = 0; i < n; i++)
            {
                arr[i] = rand() % 100000;
                cout << arr[i] << ",";
            }
            cout << endl;
            break;
        }
        case 2:
        {
            cout << "Введите 10 чисел для заполнения массива: " << endl;
             for (int i = 0; i < n; i++) {
                cin >> arr[i];
             }
            break;
        }
    }

  sort (arr, arr + n); 
  cout << endl << "Введите ключ: ";
  cin >> key;
  int l = 0;
  int r = n;
  int mid;
  while (l < r) {
    mid = (l + r) / 2;

    if (arr[mid] > key) r = mid;
    else l = mid + 1;
      
  }
  r--;
  if (arr[r] == key) cout << "Индекс элемента " << key << " в массиве равен: " << r; 
  else cout << "Извините, но такого элемента в массиве нет";
  system("pause");
  return 0;
}
