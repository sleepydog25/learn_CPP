1. [Vector-Sort](https://www.hackerrank.com/challenges/vector-sort/problem?isFullScreen=true)
```cpp

```
2. [Strings](https://www.hackerrank.com/challenges/c-tutorial-strings/problem?isFullScreen=true)
```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
	string a;
    string b;
    
    cin >> a >> b;
    
    cout << a.size()<<" "<< b.size()<<'\n';
    cout << a+b << '\n';
    cout <<b[0]<<a.substr(1)<<" "<<a[0]<<b.substr(1);
  
    return 0;
}
```
