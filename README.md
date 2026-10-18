# my_cv_learning2026.10.11
Computer Vision Learning Code Repository
for (int i = 1;i <= 9;i++)
{
	cout << i << endl;
	for (int j = 1; j <= i;j++)
	{
		cout << j << " * " << i << "=" << j * i << "  ";
		
	}cout << endl;
}
int i = 1;
while (i <= 9) {
	int j = 1;
	while (j <= i) {              
		cout << j << " * " << i << "=" << i * j << "  ";
		j++;
	}
	cout << endl;
	i++;
}
#include <iostream>
using namespace std;

class MyClass
{
public:
    void fun(int a[], int n)
    {
        int min = 0;
        for (int i = 1; i < n; i++)
        {
            if (a[i] < a[min])
            {
                min = i;
            }
        }
        int temp = a[min];
        a[min] = a[n - 1];
        a[n - 1] = temp;
    }
};

int main()
{
    int n;
    cin >> n;

    int a[100];

    for (int i = 0; i < n; i++)
    {
        cin >> a[i];
    }

    MyClass obj;
    obj.fun(a, n);

    for (int i = 0; i < n; i++)
    {
        cout << a[i] << " ";
    }

    return 0;
}
#include <iostream>
using namespace std;

class MyClass
{
public:
    void fun(int arr[], int n)
    {
        int min = 0;

        // 找最小值的下标
        for (int i = 1; i < n; i++)
        {
            if (arr[i] < arr[min])
            {
                min = i;
            }
        }

        // 交换最小值和最后一个元素
        int temp = arr[min];
        arr[min] = arr[n - 1];
        arr[n - 1] = temp;
    }
};

int main()
{
    int arr[6] = { 5, 34, 1, 2, 56, 4 };

    int n = sizeof(arr) / sizeof(arr[0]);
    cout << "交换前：";
    for (int i = 0;i < n;i++)
    {
        cout << arr[i] << "  ";
    }
    cout << endl;
    MyClass obj;
    obj.fun(arr, n);
    cout << "交换后：";
    for (int i = 0; i < n; i++)
    {
        cout << arr[i] << "  ";
    }

    return 0;
}
