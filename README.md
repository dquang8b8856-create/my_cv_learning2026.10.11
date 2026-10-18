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
