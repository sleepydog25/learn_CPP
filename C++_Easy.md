
1. [Vector-Sort](https://www.hackerrank.com/challenges/vector-sort/problem?isFullScreen=true)
```cpp
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;


int main() {
    int size;
    cin >> size;
    
    vector <int> v(size);
    for (int i =0; i<size; i++){
        cin >> v[i];
    }
    sort(v.begin(),v.end());
    
    for (int k = 0; k <size; k++){
        cout << v[k] << " ";
    }
       
    return 0;
}

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
5. [Classes and Objects](https://www.hackerrank.com/challenges/classes-objects/problem?isFullScreen=true)
```cpp
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
#include <cassert>
using namespace std;

class Student{
   private:
    
    int scores[5];
    
    public:
    
    void input(){
        for (int i=0; i<5; i++){
            cin >> scores[i];
        }
    }
    
    int calculateTotalScore(){
        int totalScore = 0 ;
        for (int j = 0; j<5; j++){
            totalScore = totalScore+scores[j];
        }
        return totalScore;
    }
};

int main() {
    int n; // number of students
    cin >> n;
    Student *s = new Student[n]; // an array of n students
    
    for(int i = 0; i < n; i++){
        s[i].input();
    }

    // calculate kristen's score
    int kristen_score = s[0].calculateTotalScore();

    // determine how many students scored higher than kristen
    int count = 0; 
    for(int i = 1; i < n; i++){
        int total = s[i].calculateTotalScore();
        if(total > kristen_score){
            count++;
        }
    }

    // print result
    cout << count;
    
    return 0;
}

```
6. [Struct](https://www.hackerrank.com/challenges/c-tutorial-struct/problem?isFullScreen=true)
```cpp
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;

struct Student{
    int age;
    string first_name;
    string last_name;
    int standard;
};

int main() {
    Student st;
    
    cin >> st.age >> st.first_name >> st.last_name >> st.standard;
    cout << st.age << " " << st.first_name << " " << st.last_name << " " << st.standard;
    
    return 0;
}
```
7. [Vector Erase](https://www.hackerrank.com/challenges/vector-erase/problem?isFullScreen=true)
```cpp
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;


int main() {
    int size ;
    cin >> size;
    vector<int>numArr;
    for (int i=0; i<size; i++){
        int x;
        cin >> x;
        numArr.push_back(x);
    }
    int index;
    int start;
    int end;
    cin >> index >> start >> end;
    
    numArr.erase(numArr.begin()+index-1);
    numArr.erase(numArr.begin()+start-1,numArr.begin()+end-1);
    
    cout << numArr.size() << "\n";
    
    for(int i=0; i<numArr.size(); i++){
        cout << numArr[i]<< " ";
    }
    return 0;
}

```
 
