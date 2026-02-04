# Introduction
1. [Say "Hello, World!" With C++](https://www.hackerrank.com/challenges/cpp-hello-world/problem?isFullScreen=true)
```cpp
#include <iostream>
#include <cstdio>
using namespace std;

int main() {
    printf("Hello, World!");
    return 0;
}
```
2. [Input and Output](https://www.hackerrank.com/challenges/cpp-input-and-output/problem?isFullScreen=true)
```cpp
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;


int main() {
    int a;
    int b;
    int c;
    cin >> a >> b >> c;
    cout << a+b+c;  
    return 0;
}
```
3. [Basic Data Types](https://www.hackerrank.com/challenges/c-tutorial-basic-data-types/problem?isFullScreen=true)
```cpp
#include <iostream>
#include <cstdio>
using namespace std;

int main(){
    int firstInput;
    long secondInput;
    char thirdInput;
    float fourthInput;
    double fifthInput;
    
    scanf("%d %ld %c %f %lf", &firstInput, &secondInput, &thirdInput, &fourthInput,&fifthInput);
    
    printf("%d\n%ld\n%c\n%f\n%lf", firstInput, secondInput, thirdInput, fourthInput, fifthInput);
    return 0;
}
```
4. [Conditional Statements](https://www.hackerrank.com/challenges/c-tutorial-conditional-if-else/problem?isFullScreen=true)
```cpp
#include <bits/stdc++.h>

using namespace std;

string ltrim(const string &);
string rtrim(const string &);



int main()
{
    string n_temp;
    getline(cin, n_temp);

    int n = stoi(ltrim(rtrim(n_temp)));

    if(n == 1){
        cout << "one";
    }else if(n == 2){
        cout << "two";
    }else if(n == 3){
        cout << "three";
    }else if (n == 4){
        cout << "four";
    }else if(n == 5){
        cout << "five";
    }else if(n == 6 ){
        cout << "six";
    }else if (n == 7){
        cout << "seven";
    }else if (n == 8){
        cout << "eight";
    }else if (n == 9){
        cout << "nine";
    }else{
        cout << "Greater than 9";
    }

    return 0;
}

string ltrim(const string &str) {
    string s(str);

    s.erase(
        s.begin(),
        find_if(s.begin(), s.end(), not1(ptr_fun<int, int>(isspace)))
    );

    return s;
}

string rtrim(const string &str) {
    string s(str);

    s.erase(
        find_if(s.rbegin(), s.rend(), not1(ptr_fun<int, int>(isspace))).base(),
        s.end()
    );

    return s;
}

```
5. [For Loop](https://www.hackerrank.com/challenges/c-tutorial-for-loop/problem?isFullScreen=true)
```cpp
#include <iostream>
#include <cstdio>
using namespace std;

int main() {
    int a;
    int b;

    cin >> a >> b;

    for (int n = a; n <= b; n++) {
        if (n == 1) {
            cout << "one" << "\n";
        } else if (n == 2) {
            cout << "two" << "\n";
        } else if (n == 3) {
            cout << "three" << "\n";
        } else if (n == 4) {
            cout << "four" << "\n";
        } else if (n == 5) {
            cout << "five" << "\n";
        } else if (n == 6) {
            cout << "six" << "\n";
        } else if (n == 7) {
            cout << "seven" << "\n";
        } else if (n == 8) {
            cout << "eight" << "\n";
        } else if (n == 9) {
            cout << "nine" << "\n";
        } else {
            if (n % 2 == 0) {
                cout << "even" << "\n";
            } else {
                cout << "odd" << "\n";
            }
        }
    }

    return 0;
}
```
6. 
7. 
