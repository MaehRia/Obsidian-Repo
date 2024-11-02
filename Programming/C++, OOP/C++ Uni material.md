---
share_link: https://share.note.sx/cmt9somh#3LN69LousQOK1LjdVsnPPCCEw3SD6OYpfVtmfJh90WM
share_updated: 2024-09-08T12:18:41+04:00
---
> [!note] 
>  Here are collected C++ Workbook and several task solutions.

![[C++ Workbook.pdf]]


## Ցիկլային ալգորիթմների կազմակերպում

```cpp
// 71

#include <iostream>
#include <cmath>

float x = 2.4, y = 0.0;

int main() {
    while (x >= 2.4 && x <= 7.6) {
        y = tan(2 * x + pow(x, 2));
        std::cout << "Output -> " << y << "    x value : " << x << std::endl;
        x += 0.2;
    }
    return 0;
}

// 72 

#include <iostream>
#include <cmath>

float x = -5.4, y = 0.0;


int main() {
    while ( x <= 1.2) {
        y = pow(tan(pow(x, 2)), 2);
        std::cout << "Output -> " << y << "   x value : " << x << std::endl;
        x += 0.4;
    }
}

// 73

#include <iostream>
#include <cmath>

double x = 7.5;
double y = 0.0;


int main()
{
    while (x >= 7.5 && x <= 12.5)
    {
        y += pow(x + 1, 2);
        std::cout << "Output step by step -> " << y << "   x value : " << x << std::endl;
        x += 0.2;
    }
}

// 74

#include <iostream>
#include <cmath>

float x = -3.8;
float y = 0.0;

int main() {
    while (x >= -3.8 && x <= 5.4) {
        y = pow(2, x + 4);
        std::cout << "Output -> " << y << "   x value: " << x << std::endl;
        x += 0.3;
    }
}

// 75

#include <iostream>
#include <cmath>

int PI = 180;
float x = ( - 1) * PI, y = 0.0;


int main() {
    while ( x <= PI) {
        y = pow(sin(x), 2) + cos(x);
        std::cout << "Output -> " << y << "   x value : " << x << std::endl;
        x += PI / 8;
    }
}

// 76

####### 1st way

#include <iostream>
#include <cmath>

float y;
int x;

int main() {

    for (int x = -5; x <= 5; x += 2) {
        if (x > 0) {
            y = pow(x, 2) + 4 * pow(x, 8);
        }
        else {
            y = 0;
        }
        std::cout << "Output-> " << y << "    x value : " << x << std::endl;
    }
    return 0;
}

####### 2nd way

#include <iostream>
#include <cmath>

int x = -5;
float y;

int main() {
    while (x >= -5 && x <= 5) {
        if (x > 0) {
            y = pow(x, 2) + 4 * pow(x, 8);
            std::cout << "Output -> " << y << "   x value : " << x << std::endl;
        }
        else {
            y = 0;
            std::cout << "Output -> " << y << "   x value : " << x << std::endl;
        }
        x += 2;
    }
}

// 77

#include <iostream>
#include <cmath>

using namespace std;

int x;
float y;

int main() {
    cout << "         Output step by step" << endl;
    for (int x = -8.8; x <= 8; x += 3) {
        if (x > 3) {
            y = pow(x, 2) + 4 * pow(x, 8);
        }
        else {
            y = 0;
        }
        cout << "Output -> " << y << "    x value: " << x << endl;
    }
    return 0;
}

// 78

#include <iostream>
#include <cmath>

using namespace std;

int x;
float y;

int main() {
    for ( int x = 10; x <= 20; x += 2) {
        if (x > 12) {
            y = 3 * (log(x) / log(3));
        }
        else {
            y = pow(x, 3);
        }
        cout << "Output -> " << y << "    x value: " << x << endl;
    }
    return 0;
}

// 79

#include <iostream>
#include <cmath>

using namespace std;

int x;
float y;

int main(){
    for (x = -4; x <= 5; x++) {
        if (x > 1) {
            y = log(x) / log(4);
        }
        else {
            y = -9;
        }
        cout << "Output -> " << y << "    x value: " << x << endl;
    }
    return 0;
}

// 80

#include <iostream>
#include <cmath>

using namespace std;

int x;
float y;

int main() {
    for (x = -5; x <= 5; x += 2) {
        if (x > 5) {
            y = pow(2, (5 - x));
        }
        else {
            y = 7 - x;
        }
        cout << "Output -> " << y << "    x value : " << x << endl;
    }
    return 0;
}

// 81

#include <iostream>
#include <cmath>

using namespace std;

float x = -7.5, y;

int main() {
    while ( x >= -7.5 && x <= 8.3) {
        y = log(pow(x, 2) + 4) / log(3);
        cout << "Output -> " << y << "    x value: " << x << endl;
        x += 0.3;
    }
    return 0;
}

// 81

#include <iostream>
#include <cmath>

using namespace std;

float x = -7.5, y;

int main() {
    while ( x >= -7.5 && x <= 8.3) {
        y = log(pow(x, 2) + 4) / log(3);
        cout << "Output -> " << y << "    x value: " << x << endl;
        x += 0.3;
    }
    return 0;
}

// 83

#include <iostream>
#include <cmath>

using namespace std;

float x, y;

int main() {
    while(x >= -4.8 && x <= 5.2) {
        y = pow(atan(x + 1), 2);
        cout << "Output -> " << y << "    x value : " << x << endl;
        x += 0.2;
    }
    return 0;
}


// 85

#include <iostream>
#include <cmath>

float y, x = -3.3;

int main() {
    while (x >= -3.3 && x <= 2.7) {
        y = abs(2 * x + pow(x, 3));
        std::cout << "Output -> " << y << "    x value : "<<x<<std::endl;
        x += 0.3;
    }
}

// 86

#include <iostream>
#include <cmath>

using namespace std;

int x;
float y;

int main() {
    while (x >= -5 && x <= 8) {
        if (x > 2) {
            y = pow(3, x + 4);
        }
        else {
            y = -8;
        }
        cout << "Output-> " << y << "   x value : " << x << endl;
        x += 2;
    }
}

// 87

#include<iostream>
#include<cmath>

using namespace std;

float x = 10, y;

int main() {
    while (x >= 10 && x <= 23) {
        if (x > 7) {
            y = exp(sin(x));
        }
        else {
            y = 0;
        }
        cout << "Output-> " << y << "    x value : " << x << endl;
        x += 3.2;
    }
    return 0;
}

// 88

###### 1st way

#include <iostream>
#include <cmath>

using namespace std;

float x = -3, y;

int main() {
    while (x >= -3 && x <= 3) {
        if (x > 1) {
            y = 6 * exp(8 + x);
        }
        else {
            y = x + 4;
        }
        cout << "Output -> " << y << "   x value : " << x << endl;
        x += 0.8;
    }
}

####### 2nd way

#include <iostream>
#include <cmath>

using namespace std;

float y, x;


int main() {
    cout << "Output step by step" << endl;
    for (float x = -3; x <= 3; x += 0.8) {
        if (x > 1) {
            y = 6 * exp(8 + x);
        }
        else {
            y = x + 4;
        }
        cout << "Output -> " << y << "    x value : " << x << endl;
    }
    return 0;
}*/

// 89

#include <iostream>
#include <cmath>

using namespace std;

float x = -5, y;

int main() {
    while (x >= -5 && x <= 9) {
        if (x > 3) {
            y = log(x) / log(4);
        }
        else {
            y = -9;
        }
        cout << "Output -> " << y << "   x value : " << x << endl;
        x += 1.5;
    }
}

// 90
#include <iostream>
#include <cmath>

float y;

int main() {
    for (float x = -30; x <= 30; x += 0.3) {
        if (x > 5) {
            y = sin(x);
        }
        else {
            y = cos(x);
        }
        std::cout << "Output -> " << y << "    x value : " << x << std::endl;
    }
}

// 91

#include <iostream>
#include <cmath>

using namespace std;

int n;
float sum = 0, x = 1.0;

int main() {
    cout << "Enter the value of n -> "; cin >> n;
    for (int i = 1; i <= n; i++) {
        sum += pow(x, 2);
        x = 0.5 * abs(x - 4);
        cout << "Output -> " << sum << endl;
    }
    return 0;
}

// 92

#include <iostream>
#include <cmath>

using namespace std;

float x = 0.5, sum = 1;
int n;

int main() {
    cout << "Enter the value of n -> "; cin >> n;
    for (int i = 1; i <= n; i++) {
        sum *= x;
        x = tan(x + 2);
        cout << "Output -> " << sum << endl;
    }
    return 0;
}

// 97

#include <iostream>
#include <cmath>

using namespace std;

int x = 1, n;
float sum = 1;

int main() {
    cout << "Enter the value of n -> "; cin >> n;
    for (int i = 0; i <= n * 3; i++) {
        sum *= x;
        x = 0.5 * x + 7;
        cout << "Output -> " << sum << endl;
    }
    return 0;
}

// 101

#include <iostream>
#include <cmath>

using namespace std;

int x = 1, y = 2, sum = 0, n;

int main() {
    cout << "Entr the value of n -> "; cin >> n;
    for (int i = 1; i <= n; i++) {
        sum += pow(x + y, 2);
        x = 2 * abs(x + 3);
        y = pow(y, 2) - 4;
        cout << "Output -> " << sum << endl;
    }
    return 0;
}

// 110

#include <iostream>
#include <cmath>

float sum = 1, a = 1, b = 1;
int n;

int main() {
    std::cout << "Enter the value of n -> "; std::cin >> n;
    int f = n * 3;
    for (int i = 1; i <= f; i++) {
        sum *= a * b;
        a = sin(a);
        b = cos(b + 3);
        std::cout << "Output -> " << sum << std::endl;
        std::cout << "# " << f << std::endl;
    }
    return 0; //shotouts to Galy 
}

//236 

#include <iostream>

using namespace std;

int arr[8] = { 0 }, sum = 1, evenCount = 0;  // Changed 'count' to 'evenCount'

int main() {
    for (int i = 0; i < 8; i++) {  // Fix the loop to avoid accessing arr[8]
        cout << "Enter value for arr[" << i << "] -> ";
        cin >> arr[i];

        if (arr[i] % 2 == 0) {  // Check if the current element is even
            evenCount++;  // Increment evenCount for even numbers
            sum *= arr[i];  // Multiply sum by the even number
        }
    }
    cout << "Sum of even numbers: " << sum << endl;
    cout << "Count of even numbers: " << evenCount << endl;  // Output evenCount

    return 0;
}
```


## Միաչափ զանգվածներ

```cpp
// 215

#include <iostream>

using namespace std;

int n;
int arr[];
int sum = 0;

int main() {
	cout << " items number -> "; cin >> n;
	for (int i = 0; i < n; i++) {
		cout << i << " number -> " << endl; cin >> arr[i];
	}
	for (int i = 0; i < n; i++) {
		if (i % 2 == 0) {
			sum += arr[i];
		}
	}
}

// 311

#include <iostream>

using namespace std;

int main() {
    int n;
    int count = 0;
    int max = 0;
    int g = 0;

    cout << "Enter the size of array : "; cin >> n;
    int* arr = new int[n];
    for (int i = 0; i < n; i++) {
        arr[i] = rand() % 21 - 10;
        if (arr[i] >= 0) {
            count++;
        }
        cout << arr[i] << " ";
    }
    cout << endl;
    cout << "Positive numbers -> " << count << endl;
    max = arr[0];
    for (int i = 1; i < n; i++) {
        if (max < arr[i]) {
            max = arr[i];
        }
    }
    cout << "max = " << max << endl;

    int* arr1 = new int[count];
    for (int i = 0; i < n; i++) {
        if (arr[i] >= 0) {
            arr1[g++] = arr[i] + max;
        }
    }
    for (int i = 0; i < count; i++) {
        cout << arr1[i] << " ";
    }
}

// 312

####### 1st way

#include<iostream>

int main() {
    int n;

    std::cout << "length =";
    std::cin >> n;
    int* arr = new int[n];
    for (int i = 0; i < n; i++) {
        arr[i] = rand() % 20 - 10;
        std::cout << arr[i] << " ";
    }
    std::cout << "\n";
    int len = n / 2;
    int* arr1 = new int[len]; 
    int j = 0;
    for (int i = 0; i < n; i += 2) {
        if (abs(arr[i] > arr[i + 1])) {
            arr[j] = arr[i];
        }
        else {
            arr1[j] = arr[i + 1];
        }
        j++;
    }
    for (int i = 0; i < len; i++) {
        std::cout << arr[i] << " ";
    }
    delete[] arr, arr1;
    return 0; 
}

####### 2nd way

#include <iostream>

using namespace std;

int main() {
    int n; 
    cout << "Enter the size of array -> "; cin >> n;
    int* arr = new int[n];
    for (int i = 0; i < n; i++) 
    {
        arr[i] = rand() % 20 - 10;
        cout << arr[i] << " ";
    }
    cout << endl;
    int k = n / 2;
    int* arr1 = new int[k];
    int j = 0;
    for (int i = 0; i < n; i += 2)
    {
        if (abs(arr[i]) > abs(arr[i] + 1))
        {
            arr1[j] = arr[i];
        }
        else {
            arr1[j] = arr[i + 1];
        }
        cout << arr1[j] << " ";
    }
}*/

// 315 -----------

#include <iostream>

using namespace std;

int main()
{
    int n;
    cout << "Enter array size -> "; cin >> n;
    int* arr = new int[n];
    for (int i = 0; i < n; i++) {
        arr[i] = rand() % 20 - 10;
        cout << arr[i] << " ";
    }

}

// 318

#include <iostream>

using namespace std;

int main() {
    int n = 0;
    cout << "Enter array size -> "; cin >> n;
    int* arr = new int[n];
    for (int i = 0; i < n; i++) 
    {
        arr[i] = rand() % 21 - 10;
        cout << arr[i] << " ";
    }
    cout << endl;
    int* new_arr = new int[n];
    int g = 0;

    for (int i = 0; i < n; i++) 
    {
        if (arr[i] < 0)
            new_arr[g++] = arr[i];
    }

    for (int i = 0; i < n; i++) 
    {
        if (arr[i] > 0)
            new_arr[g++] = arr[i];
    }

    for (int i = 0; i < n; i++)
    {
        cout << "Output index -> [" << i << "] : " << new_arr[i]<<endl;
    }
    
}

// 319

#include <iostream>

using namespace std;

int main() {
    int n;
    cout << "Enter array size -> "; cin >> n;
    int* arr = new int[n];
    for (int i = 0; i < n; i++)
    {
        arr[i] = rand() % 20 - 10;
        cout << arr[i] << " ";
    }
    cout << endl;
    int max = arr[0];
    int index = 0;
    int* new_arr = new int[n];
    for (int i = 0; i < n; i++) {
        if (arr[i] > max) {
            max = arr[i];
        }
    }
    for (int i = 0; i < n; i++)
        new_arr[index++] = arr[i] + max;
    for (index = 2; index < n; index += 3)
        new_arr[index] = 0;
    cout << endl;
    for (int i = 0; i < n; i++)
        cout << new_arr[i] << " ";
}


// 313

###### 1st way

include <iostream>

using namespace std;

int main() {
    int n;
    cout << "Enter array size -> "; cin >> n;
    int* arr = new int[n];
    int* arr1 = new int[n];
    for (int i = 0; i < n; i++) {
        arr[i] = rand() % 30 - 10;
        cout << arr[i] << " ";
    }
    cout << endl;
    arr1[0] = arr[0];
    int index = 0;
    for (int i = 1; i < n; i++) {
        if (i % 2 == 0) {
            arr1[index] = arr[i - 1];
        }
        else {
            arr1[index] = arr[i + 1];
        }
    }
}

###### 2nd way

#include <iostream>
#include <cmath>
using namespace std;
int main() {

    int k = 0, len = 0, index = 1;
    cout << "Enter odd number k -> ";
    cin >> k;
    int* arr = new int[k];
    len = k;
    int* arr1 = new int[len];
    for (int i = 0; i < k; i++) {
        arr[i] = rand() % 30 - 15;
        cout << arr[i] << " ";
    }
    arr1[0] = arr[0];
    for (int i = 1; i < k; i++) {
        if (i % 2 == 0) {
            arr1[index] = arr[i - 1];
        }
        else {
            arr1[index] = arr[i + 1];
        }
        index++;
    }
    cout << endl;

    for (int i = 0; i < len; i++) {
        cout << arr1[i] << " ";
    }
    delete[] arr1;
    delete[] arr;
    return 0;
}
```


## Երկչափ զանգված

```cpp
// 588

#include <iostream>

using namespace std;

int main() {
	int n;
	cout << "Enter matrix -> "; cin >> n;
	int** arr = new int* [n];
	for (int i = 0; i < n; i++) {
		arr[i] = new int[n];
	}
	for (int i = 0; i < n; i++) {
		for (int j = 0; j < n; j++) {
			arr[i][j] = rand() % 10;
			cout << arr[i][j] << " ";
		}
		cout << endl;
	}
	for (int i = 0; i < n-1; i++) {
		for (int j = 0; j < n-i-1; j++) {
			arr[i][j] = 1;
		}
		
	}
	cout << "\n";
	for (int i = 0; i < n; i++) {
		for (int j = 0; j < n; j++) {
			cout << arr[i][j] << " ";
		}
		cout << endl;
	}
	for (int i = 0; i < n; i++) {
		delete[] arr[i];
	}
	delete[] arr;
}

// 509

#include <iostream>

using namespace std;

int main() {
	int n;
	cout << "Enter matrix size -> ";
	cin >> n;

	// spacing
	char** arr = new char* [n];
	for (int i = 0; i < n; i++) {
		arr[i] = new char[n];
	}

	// valuing & printing
	int count = 0;
	for (int i = 0; i < n; i++) {
		for (int j = 0; j < n; j++) {
			// arr[i][j] = rand() % 26 + 'A'; // for uppercase letters
			arr[i][j] = rand() % 26 + 'a'; // for lowercase letters
			cout << arr[i][j] << "\t";
			if (arr[i][j] == 'a') {
				count++;
			}
		}
		cout << endl;
	}
	cout << "\n";
	cout << "count = " << count;

	// Free memory
	for (int i = 0; i < n; i++) {
		delete[] arr[i];
	}
	delete[] arr;

	return 0;
}

// 516

#include <iostream>

using namespace std;

int main() {
	int m, n;
	cout << "Enter the value of m -> "; cin >> m;
	cout << "Enter the value of n -> "; cin >> n;
	int** arr = new int* [m];
	for (int i = 0; i < m; i++) 
		arr[i] = new int[n];
	
}
```

## Structures

```cpp
// 724

#include <iostream>
#define students 3

using namespace std;

struct group {
	string name;
	string surname;
	int absents;
};
int main() {
	group blank[students];
	for (int i = 0; i < students; i++) {
		cout << "Enter " << i << " student's name ->"; cin >> blank[i].name;
		cout << "Enter " << i << " student's surname ->"; cin >> blank[i].surname;
		cout << "Enter " << i << " student's amount of absents ->"; cin >> blank[i].absents;
	}
	cout << endl;
	int max = blank[0].absents;
	for (int i = 1; i < students; i++) {
		if (max < blank[i].absents)
			max = blank[i].absents;
	}
	for (int i = 0; i < students; i++) {
		if (max == blank[i].absents) {
			cout << "Name: " << blank[i].name << "\t" << "Surname: " << blank[i].surname;
		}
	}
}

// 725

#include <iostream>
#define students 3

using namespace std;

struct group {
	string name;
	string surname;
	int exam;
};

int main() {
	group blank[students];
	for (int i = 0; i < students; i++) {
		cout << "Enter " << i+1 << " student's name ->"; cin >> blank[i].name;
		cout << "Enter " << i+1 << " student's surname ->"; cin >> blank[i].surname;
		cout << "Enter " << i+1 << " student's exam grade ->"; cin >> blank[i].exam;
	}
	cout << endl;
	int mid = (blank[0].exam + blank[1].exam + blank[2].exam) / students;
	for (int i = 0; i < students; i++) {
		if (mid < blank[i].exam)
			cout << "Name: " << blank[i].name << "\t" << "Surname: " << blank[i].surname;
	}
}

// 726

#include <iostream>
#define students 3

using namespace std;

struct group{
	string name;
	string surname;
	int exam;
};

int main() {
	int ratting_range[2] = { 10, 20 };
	group blank[students];
	for (int i = 0; i < students; i++) {
		cout << "Enter " << i + 1 << " student's name ->"; cin >> blank[i].name;
		cout << "Enter " << i + 1 << " student's surname ->"; cin >> blank[i].surname;
		cout << "Enter " << i + 1 << " student's exam grade ->"; cin >> blank[i].exam;
	}
	cout << endl;
	for (int i = 0; i < students; i++) {
		if (blank[i].exam > 10)
			cout << "Name: " << blank[i].name << "\t" << "Surname: " << blank[i].surname << endl;
	}
}

// 727

#include <iostream>
#define students 3

using namespace std;

struct group {
	string surname;
	int number;
	int grade;
};

int main() {
	group blank[students];
	for (int i = 0; i < students; i++) {
		cout << "Enter " << i + 1 << " student's surname ->"; cin >> blank[i].surname;
		cout << "Enter " << i + 1 << " student's number ->"; cin >> blank[i].number;
		cout << "Enter " << i + 1 << " student's grade ->"; cin >> blank[i].grade;
	}
	for (int i = 0; i < students; i++) {
		if (blank[i].grade <= 9)
			cout << "number: " << blank[i].number << "\t" << "surname: " << blank[i].surname << endl;
	}
}

// 728

#include <iostream>
#define workers 3

using namespace std;

struct group {
	string surname;
	string name;
	int status;
	int kids;
};

int main() {
	group blank[workers];
	for (int i = 0; i < workers; i++) {
		cout << "Enter N" << i + 1 << " worker's surname ->"; cin >> blank[i].surname;
		cout << "Enter N" << i + 1 << " worker's name ->"; cin >> blank[i].name;
		cout << "Enter N" << i + 1 << " worker's status ->"; cin >> blank[i].status;
		cout << "Enter N" << i + 1 << " worker's kids amount ->"; cin >> blank[i].kids;
	}
	for (int i = 0; i < workers; i++) {
		if (blank[i].status == 1 && blank[i].kids > 0)
			cout << "name: " << blank[i].name << "\t" << "surname: " << blank[i].surname << endl;
	}
}

// 729

#include <iostream>
#define employees 3

using namespace std;

struct group {
	string surname;
	int kids;
};

int main(){
	group blank[employees];
	for (int i = 0; i < employees; i++) {
		cout << "Enter N" << i + 1 << " employee's surname -> "; cin >> blank[i].surname;
		cout << "Enter N" << i + 1 << " employee's kids -> "; cin >> blank[i].kids;
	}
	for (int i = 0; i < employees; i++) {
		if (blank[i].kids > 0)
			cout << "surname: " << blank[i].surname << "\t" << "kids: " << blank[i].kids << endl;
	}
}

// 730

#include <iostream>
#define students 3

using namespace std;

struct group{
	string surname;
	int gpa;
	int number;
};

int main() {
	int ratting_range[2] = { 40, 80 };
	group blank[students];
	for (int i = 0; i < students; i++) {
		cout << "Enter N" << i + 1 << " student's surname ->"; cin >> blank[i].surname;
		cout << "Enter N" << i + 1 << " student's gpa ->"; cin >> blank[i].gpa;
		cout << "Enter N" << i + 1 << " student's number ->"; cin >> blank[i].number;
	}
	cout << endl;
	for (int i = 0; i < students; i++) {
		if (blank[i].gpa >= ratting_range[0] && blank[i].gpa <= ratting_range[1])
			cout << "number: " << blank[i].number << "\t" << "surname: " << blank[i].surname;
	}
}

// 731

#include <iostream>
#define employees 3

using namespace std;

struct group {
	string surname;
	int fam;
	int salary;
};

int main() {
	group blank[employees];
	int mid;
	int G;
	cout << "Enter G ->"; cin >> G;
	for (int i = 0; i < employees; i++) {
		cout << "Enter N" << i + 1 << " worker's surname ->"; cin >> blank[i].surname;
		cout << "Enter N" << i + 1 << " worker's family members ->"; cin >> blank[i].fam;
		cout << "Enter N" << i + 1 << " worker's salary ->"; cin >> blank[i].salary;
		mid = blank[i].salary / blank[i].fam;
		cout << "mid = " << mid << endl;
	}
	cout << endl;
	for (int i = 0; i < employees; i++) {
		if (mid < G)
			cout << "surname: " << blank[i].surname << endl;
	}
}

// 732 

#include <iostream>
#define students 3

using namespace std;

struct group{
	char surname[20];
	string name;
	string second_name;
};

int main() {
	group blank[students];
	for (int i = 0; i < students; i++) {
		cout << "Enter N" << i + 1 << " student's surname ->"; cin >> blank[i].surname;
		cout << "Enter N" << i + 1 << " student's name ->"; cin >> blank[i].name;
		cout << "Enter N" << i + 1 << " student's second name ->"; cin >> blank[i].second_name;
	}
	for (int i = 0; i < students; i++) {
		int lenght = strlen(blank[i].surname);
		if (blank[i].surname[0] == 'A' && blank[i].surname[lenght - 1] == 'n') {
			cout << blank[i].surname << " " << blank[i].name << " " << blank[i].second_name << endl;
		}
	}
}

// 734

#include <iostream>
#define workers 3

using namespace std;

struct group {
	int kids;
	int midS;
};

int main() {
	group blank[workers];
	int salary_range;
	int count = 0;
	cout << "Enter salary range -> "; cin >> salary_range;
	for (int i = 0; i < workers; i++) {
		cout << "Enter N" << i + 1 << " worker's kids count ->"; cin >> blank[i].kids;
		cout << "Enter N" << i + 1 << " worker's mid salary ->"; cin >> blank[i].midS;
	}
	for (int i = 0; i < workers; i++) {
		if (blank[i].midS < salary_range) {
			count += blank[i].kids;
		}
	}
	cout << "count = " << count;
}

// 735

#include <iostream>
#define students 3

using namespace std;

struct group {
	string surname;
	int ratting_mark;
	int exam;
};

int main() {
	group blank[students];
	for (int i = 0; i < students; i++) {
		cout << "Enter N" << i + 1 << " student's surname ->"; cin >> blank[i].surname;
		cout << "Enter N" << i + 1 << " student's ratting mark ->"; cin >> blank[i].ratting_mark;
		cout << "Enter N" << i + 1 << " student's exam grade ->"; cin >> blank[i].exam;
	}
	int k;
	cout << "Enter K ->"; cin >> k;
	for (int i = 0; i < students; i++) {
		if (abs(blank[i].ratting_mark - blank[i].exam) < k)
			cout << "surname: " << blank[i].surname << endl;
	}
}

// 736

#include <iostream>
#define students 3

using namespace std;

struct group {
	string surname;
	int ratting_mark;
	int exam;
	int final_grade;
};

int main() {
	group blank[students];
	for (int i = 0; i < students; i++) {
		cout << "Enter N" << i + 1 << " student's surname  ->"; cin >> blank[i].surname;
		cout << "Enter N" << i + 1 << " student's ratting mark (0-20) ->"; cin >> blank[i].ratting_mark;
		cout << "Enter N" << i + 1 << " student's exam grade (0-20) ->"; cin >> blank[i].exam;
		blank[i].final_grade = (blank[i].exam + blank[i].ratting_mark);
		cout << "final grade = " << blank[i].final_grade;
		cout << endl;
	}
	for (int i = 0; i < students; i++) {
		if (5 < blank[i].ratting_mark < 10 && 10 < blank[i].final_grade < 20)
			cout << "surname : " << blank[i].surname<<endl;
	}
}

// 737

#include <iostream>
#define students 3

using namespace std;

struct group {
	int pension;
	int grade;
};

int main() {
	group blank[students];
	for (int i = 0; i < students; i++) {
		cout << "Enetr N" << i + 1 << " student's pension ->"; cin >> blank[i].pension;
		cout << "Enetr N" << i + 1 << " student's grade ->"; cin >> blank[i].grade;
	}
	int k;
	int mid = 0;
	cout << "Enter k (0-20)-> "; cin >> k;
	for (int i = 0; i < students; i++) {
		mid += blank[i].grade;
	}
	mid /= students;
	for (int i = 0; i < students; i++) {
		if (mid > k) {
			blank[i].pension *= 2;
			cout << "pension = " << blank[i].pension << endl;
		}
		else {
			cout << "pension = " << blank[i].pension << endl;
		}
	}
}

// 739

#include <iostream>
#define students 3

using namespace std;

struct group {
	string surname;
	int number;
	int exam;
};

int main() {
	group blank[students];
	for (int i = 0; i < students; i++) {
		cout << "Enter N" << i + 1 << " student's surname -> "; cin >> blank[i].surname;
		cout << "Enter N" << i + 1 << " student's exam grade -> "; cin >> blank[i].exam;
		cout << "Enter N" << i + 1 << " student's number -> "; cin >> blank[i].number;
	}
	int k;
	cout << "Enter k (0-20) -> "; cin >> k;
	for (int i = 0; i < students; i++) {
		if (10 < blank[i].number<20 && blank[i].exam>k)
			cout << "surname : " << blank[i].surname << endl;
	}
}

// 741

#include <iostream>
#define students 4

using namespace std;

struct group {
	string name; 
	string surname;
	int number;
};

int main() {
	group blank[students];
	for (int i = 0; i < students; i++) {
		cout << "Enter N" << i + 1 << " student's name -> "; cin >> blank[i].name;
		cout << "Enter N" << i + 1 << " student's surname -> "; cin >> blank[i].surname;
		cout << "Enter N" << i + 1 << " student's number -> "; cin >> blank[i].number;
	}
	for (int i = 0; i < students; i++) {
		if (blank[i].name[0] == 'A' && blank[i].surname[0] == 'A') {
			if (blank[i].number >= 11 && blank[i].number <= 20) {
				cout << "name: " << blank[i].name << "\t" << "surname: " << blank[i].surname << endl;
			}
		}
	}
}

// 742

#include <iostream>
#define paragraphs 4

using namespace std;


struct group {
	string author;
	int pages;
};

int main() {
	group blank[paragraphs];
	for (int i = 0; i < paragraphs; i++) {
		cout << "Enter N" << i + 1 << " author's name -> "; cin >> blank[i].author;
		cout << "Enter N" << i + 1 << " author's book's amount of pages -> "; cin >> blank[i].pages;
	}
	int count = 0;
	for (int i = 0; i < paragraphs; i++) {
		if (blank[i].author[0] == 'A') {
			count += blank[i].pages;
		}
	}
	cout << "pages = " << count;
}

// 745

#include <iostream>
#define programs 4

using namespace std;

struct group {
	string title;
	int hour = 0;
	int min = 0;
};

int main() {
	group blank[programs];
	for (int i = 0; i < programs; i++) {
		cout << "Enter N" << i + 1 << " program title -> "; cin >> blank[i].title;
		cout << "Enter N" << i + 1 << " program time(hour) -> "; cin >> blank[i].title;
		cout << "Enter N" << i + 1 << " program title(minutes) -> "; cin >> blank[i].title;

	}
	for (int i = 0; i < programs; i++) {
		if (blank[i].hour == 18 && blank[i].min == 20) {
			cout << "Program title: " << blank[i].title << endl;
		}
	}
}

```

## Functions

```cpp
// 596

#include <iostream>

using namespace std;

int max(int, int, int);

int main() {
	int a, b, y;
	cout << "Enter the value of a -> "; cin >> a;
	cout << "Enter the value of b -> "; cin >> b;
	y = max(a, a + b, a - b) + max(b, 2 * b - a, b + 2 * a);
	cout << "y = " << max(a, a + b, a - b) << "+" << max(b, 2 * b - a, b + 2 * a) << "=" << y;
}

int max(int k1, int k2, int k3) {
	int max = k1;
	if (max < k2)
		max = k2;
	if (max < k3)
		max = k3;
	return max;
}

// 597

#include <iostream>

using namespace std;

int min(int, int, int);

int main() {
	int a, b, c, y;
	cout << "Enter the value of a-> "; cin >> a;
	cout << "Enter the value of b-> "; cin >> b;
	cout << "Enter the value of c-> "; cin >> c;
	y = min(3 * a, 2 * b, c) * min(a, b, 3 * c);
	cout << "y = " << min(3 * a, 2 * b, c) << " * " << min(a, b, 3 * c) << " = " << y;
}

int min(int k1, int k2, int k3) {
	int min = k1;
	if (min > k2)
		min = k2;
	if (min > k3)
		min = k3;
	return min;
}

// 598

#include <iostream>

using namespace std;

int max(int, int, int);

int main() {
	int a, b, y;
	cout << "Enter the value of a-> "; cin >> a;
	cout << "Enter the value of b-> "; cin >> b;
	y = max(5, a, b) + max(7, b, a + b);
	cout << "y = " << max(5, a, b) << " + " << max(7, b, a + b) << " = " << y;
}

int max(int k1, int k2, int k3) {
	int max = k1;
	if (max < k2)
		max = k2;
	if (max < k3)
		max = k3;
	return max;
}

// 599

#include <iostream>

using namespace std;

int max(int, int, int);

int main() {
	int a, b, c, y;
	cout << "Enter the value of a-> "; cin >> a;
	cout << "Enter the value of b-> "; cin >> b;
	cout << "Enter the value of c-> "; cin >> c;
	y = pow(max(5+a, b, 3), 2) * max(3+a, b, c);
	cout << "y = " << pow(max(5 + a, b, 3), 2) << " * " << max(3 + a, b, c) << " = " << y;
}

int max(int k1, int k2, int k3) {
	int max = k1;
	if (max < k2)
		max = k2;
	if (max < k3)
		max = k3;
	return max;
}

// 600 

#include <iostream>

using namespace std;

int min(float, float, float);

int main() {
	float a, b, c, y;
	cout << "Enter the value of a -> "; cin >> a;
	cout << "Enter the value of b -> "; cin >> b;
	cout << "Enter the value of c -> "; cin >> c;
	y = pow(min(3.4 + 5 * a, b, c) + min(0.5, a, c), 2);
	cout << "y = (" << min(3.4 + 5 * a, b, c) << " + " << min(0.5, a, c) << ")^2 = " << y;
}

int min(float k1, float k2, float k3) {
	int min = k1;
	if (min > k2)
		min = k2;
	if (min > k3)
		min = k3;
	return min;
}

// 601

#include <iostream>

using namespace std;

int max(int, int, int);

int main() {
	int a, b, c, y;
	cout << "Enter the value of a ->"; cin >> a;
	cout << "Enter the value of b ->"; cin >> b;
	cout << "Enter the value of c ->"; cin >> c;
	y = max(3, a + b, c) - max(a + b, b + c, a + c);
	cout << "y = " << max(3, a + b, c) << " - " << max(a + b, b + c, a + c) << " = " << y;
}

float max(int k1, int k2, int k3) {
	int max = k1;
	if (max < k2)
		max = k2;
	if (max < k3)
		max = k3;
	return max;
}

//602

#include <iostream>
#include <cmath>

using namespace std;

int min(int, int, int);

int main() {
	int a, b, c;
	float y;
	cout << "Enter the value of a -> "; cin >> a;
	cout << "Enter the value of b -> "; cin >> b;
	cout << "Enter the value of c -> "; cin >> c;
	y = exp(min(2, a + b, b + c) + min(a, b, c));
	cout << "y = exp(" << min(2, a + b, b + c) << " + " << min(a, b, c) << ") = " << y;
}

int min(int k1, int k2, int k3) {
	int min = k1;
	if (min > k2)
		min = k2;
	if (min > k3)
		min = k3;
	return min;
}

// 603

#include <iostream>

using namespace std;

int max(int, int, int);

int main() {
	int x, y =0, z;
	cout << "Enter the value of x -> "; cin >> x;
	cout << "Enter the value of y -> "; cin >> y;
	cout << "Enter the value of z -> "; cin >> z;
	int num1 = max(x, x + 1, x + y + z);
	int num2 = max(x, z, y - 1);
	sum = pow(max(x, x + 1, x + y + z) - max(x, z, y - 1), 2);
	cout << "y = (" << max(x, x + 1, x + y + z) << " - " << max(x, z, y - 1) << ")^2 = " << sum;
}

int max(int k1, int k2, int k3) {
	int max = k1;
	if (max < k2)
		max = k2;
	if (max < k3)
		max = k3;
	return max;
}

// 604

#include <iostream>
#include <cmath>

using namespace std;

int min(int, int, int);

float main() {
	float x, y, z, a, b, c, sum;
	cout << "Enter the value of x -> "; cin >> x;
	cout << "Enter the value of y -> "; cin >> y;
	cout << "Enter the value of z -> "; cin >> z;
	cout << "Enter the value of a -> "; cin >> a;
	cout << "Enter the value of b -> "; cin >> b;
	cout << "Enter the value of c -> "; cin >> c;
	sum = sin(min(x, x + 1, x + y + z)) + cos(min(5, b + c, a));
	cout << "y = " << sin(min(x, x + 1, x + y + z)) << " + " << cos(min(5, b + c, a)) << " = " << sum;
}

int min(int k1, int k2, int k3) {
	int min = k1;
	if (min > k2)
		min = k2;
	if (min > k3)
		min = k3;
	return min;
}

// 605

#include <iostream>
#include <cmath>

using namespace std;

int min(int, int, int);

float main() {
	float x, y, sum;
	cout << "Enter the value of x -> "; cin >> x;
	cout << "Enter the value of y -> "; cin >> y;
	sum = tan(min(x, y, x + y) - min(2, x, x - y));
	cout << "y = " << y;
}

int min(int k1, int k2, int k3) {
	int min = k1;
	if (min > k2)
		min = k2;
	if (min > k3)
		min = k3;
	return min;
}
```


## Random 

Task N1:

- **Create a dynamically allocated 2D array** (matrix) with dimensions `n` x `m` using dynamic memory allocation (`new`).
- **Fill the matrix with random integers** within a certain range (in this case, between -10 and 9).
- **Calculate the sum of each row** of the matrix.
- **Store these sums in a 1D array** (or vector) and print the results.

```cpp
#include <iostream>

using namespace std;

int main()
{

	int n = 0; cin >> n;
	int m = 0; cin >> m;
	int** arr = new int* [n];
	for (int i = 0; i < n; i++) {
		arr[i] = new int[m];
	}

	for (int i = 0; i < n; i++) {
		for (int j = 0; j < m; j++) {
			arr[i][j] = rand() % 20 - 10;
			cout << arr[i][j] << "\t";
		}
		cout << endl;
	}

	int* vector = new int[n];
	int index = 0;
	int sum = 0;

	for (int i = 0; i < n; i++) {
		for (int j = 0; j < m; j++) {
			sum += arr[i][j];
		}
		vector[index++] = sum;
		sum = 0;
	}
	for (int i = 0; i < n; i++) {
		cout << vector[i] << ' ';
	}
	return 0;
}
```

Task N2:

- The user is prompted to input **10 numbers**, which are stored in an array (`arr`).
- The array is **sorted in ascending order** using the `sort` function from the C++ Standard Library.
- The user is asked to input a **key** (the number they want to search for in the array).
- **Binary Search**:
- A **binary search** algorithm is then applied to the sorted array to check if the key exists in the array:
   - If the key is found, the program prints the **index** of the key in the array.
   - If the key is not found, the program informs the user that the element doesn't exist in the array. 

```cpp
#include <iostream>
#include <algorithm>

using namespace std;

int main() {
	int arr[10]; // ստեղծում ենք 10 էլեմենտով զանգված
	int key; // ստեղծում ենք բանալի էլեմենտը

	cout << "Enter 10 numbers :" << endl;

	for (int i = 0; i < 10; i++) {
		cout << i + 1 << " -> "; cin >> arr[i]; // ներ ենք մուծում անդամնեևը
	}

	sort(arr, arr + 10); // էլեմենտների դասավորում ըստ աճման կարգի sort ֆունկցիայով

	cout << endl << "Enter key : "; cin >> key;

	bool flag = false;
	int l = 0; // ձախ սահման
	int r = 9; // աջ սահման
	int mid;

	while ((l <= r) && (flag != true)) {
		mid = (l + r) / 2; //  [l,r] միյակայքի միջին անդամի ստեղծում

		if (arr[mid] == key)  flag = true ; // բանալի տարրը համեմատում ենք mid-ի հետ
		if (arr[mid] > key)  r = mid - 1 ; // ստուգում ենք թե mid-ից որ կողմ ընկած տարրերը հարկավոր չեն
		else  l = mid + 1 ;
	}

	if (flag) cout << "The index of " << key << " in array is equal to :  " << mid;
	else cout << "Sorry, but such element doesn't exist in array.";

	return 0;
}
```
