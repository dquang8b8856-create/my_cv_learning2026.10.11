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
	ruturn;
	}
#include <iostream>
#include <vector>
#include <algorithm>
using namespace std;

int main()
{
    int n;
    cin >> n;

    vector<int> arr;

    
    for (int i = 0; i < n; i++)
    {
        int x;
        cin >> x;
        arr.push_back(x);
    }

    
    sort(arr.begin(), arr.end());

    for (int i = 0; i < arr.size(); i++)
    {
        cout << arr[i] << " ";
    }
    cout << endl;

    
    vector<int> result;

    if (!arr.empty())
    {
        result.push_back(arr[0]);

        for (int i = 1; i < arr.size(); i++)
        {
            if (arr[i] != arr[i - 1])
            {
                result.push_back(arr[i]);
            }
        }
    }

    for (int i = 0; i < result.size(); i++)
    {
        cout << result[i] << " ";
    }
    cout << endl;

    return 0;

}
#include <iostream>
#include <sstream>
#include <string>
#include <vector>
using namespace std;

int main()
{
    string s;
    getline(cin, s);

    stringstream ss(s);
    string word;
    vector<string> words;

    while (ss >> word)
    {
        words.push_back(word);
    }

    cout << "单词数量：" << words.size() << endl;

    for (int i = words.size() - 1; i >= 0; i--)
    {
        cout << words[i] << " ";
    }

    cout << endl;

    return 0;

}
#include <iostream>
#include <string>
using namespace std;

class Student
{
private:
    string name;
    string id;
    int* scores;
    int numScores;

public:
    
    Student(string n, string i, int num, int s1, int s2, int s3)
    {
        name = n;
        id = i;
        numScores = num;

        scores = new int[numScores];

        scores[0] = s1;
        scores[1] = s2;
        scores[2] = s3;
    }

    
    Student(const Student& other)
    {
        name = other.name;
        id = other.id;
        numScores = other.numScores;

        scores = new int[numScores];

        for (int i = 0; i < numScores; i++)
        {
            scores[i] = other.scores[i];
        }
    }

    
    ~Student()
    {
        delete[] scores;
    }

  
    void print()
    {
        cout << name << " " << id << " ";

        for (int i = 0; i < numScores; i++)
        {
            cout << scores[i] << " ";
        }

        cout << endl;
    }

    
    void setScore(int index, int score)
    {
        if (index >= 0 && index < numScores)
        {
            scores[index] = score;
        }
    }
};

int main()
{
    Student stu1("张三", "2025001", 3, 85, 90, 78);

    Student stu2 = stu1;

    cout << "复制前：" << endl;
    cout << "stu1：";
    stu1.print();

    cout << "stu2：";
    stu2.print();

    stu1.setScore(0, 60);

    cout << "\n修改 stu1 第一门成绩后：" << endl;
    cout << "stu1：";
    stu1.print();

    cout << "stu2：";
    stu2.print();

    return 0;
}
