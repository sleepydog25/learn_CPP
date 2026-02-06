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
3. [StringStream](https://www.hackerrank.com/challenges/c-tutorial-stringstream/problem?isFullScreen=true)
```cpp
#include <sstream>
#include <vector>
#include <iostream>
using namespace std;

vector<int> parseInts(string str) {
	stringstream ss (str);
    vector<int> integers;
    int x;
    char ch;
    while (ss >> x){
      integers.push_back(x);
      ss >> ch;  
    } 
    return integers;
}

int main() {
    string str;
    cin >> str;
    vector<int> integers = parseInts(str);
    for(int i = 0; i < integers.size(); i++) {
        cout << integers[i] << "\n";
    }
    
    return 0;
}
```
4. [Class](https://www.hackerrank.com/challenges/c-tutorial-class/problem?isFullScreen=true)
```cpp
#include <iostream>
#include <sstream>
using namespace std;

class Student{
    private:
    int age;
    int standard;
    string first_name;
    string last_name;
    
    public :
    void set_age (int a){
        age = a;
    }
    void set_standard(int s){
        standard = s;
    }
    void set_first_name(string f){
        first_name = f;
    }
    void set_last_name(string l){
        last_name = l;
    }
    
    int get_age(){
        return age;
    }
    string get_first_name(){
        return first_name;
    }
    int get_standard(){
        return standard;
    }
    string get_last_name(){
        return last_name;
    }
    string to_string(){
        stringstream ss;
        ss<<age<<","<<first_name<<","<<last_name<<","<<standard;
        return ss.str();
    }
};

int main() {
    int age, standard;
    string first_name, last_name;
    
    cin >> age >> first_name >> last_name >> standard;
    
    Student st;
    st.set_age(age);
    st.set_standard(standard);
    st.set_first_name(first_name);
    st.set_last_name(last_name);
    
    cout << st.get_age() << "\n";
    cout << st.get_last_name() << ", " << st.get_first_name() << "\n";
    cout << st.get_standard() << "\n";
    cout << "\n";
    cout << st.to_string();
    
    return 0;
}
```
5. 
