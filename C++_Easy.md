
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
8. [Inheritance Introduction](https://www.hackerrank.com/challenges/inheritance-introduction/problem?isFullScreen=true)
 ```cpp
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;


class Triangle{
    public:
    	void triangle(){
     		cout<<"I am a triangle\n";
    	}
};

class Isosceles : public Triangle{
    public:
    	void isosceles(){
    		cout<<"I am an isosceles triangle\n";
    	}
  		void description(){
            cout << "In an isosceles triangle two sides are equal\n";
        }
};

int main(){
    Isosceles isc;
    isc.isosceles();
  	isc.description();
    isc.triangle();
    return 0;
}
```
9. [Multi Level Inheritance](https://www.hackerrank.com/challenges/multi-level-inheritance-cpp/problem?isFullScreen=true)
```cpp
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;

class Triangle{
	public:
		void triangle(){
			cout<<"I am a triangle\n";
		}
};

class Isosceles : public Triangle{
  	public:
  		void isosceles(){
    		cout<<"I am an isosceles triangle\n";
  		}
};

class Equilateral : public Isosceles{
    public:
    void equilateral(){
        cout << "I am an equilateral triangle\n";
    }
};

int main(){
  
    Equilateral eqr;
    eqr.equilateral();
    eqr.isosceles();
    eqr.triangle();
    return 0;
}

```
10. [Lower Bound-STL](https://www.hackerrank.com/challenges/cpp-lower-bound/problem)
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

    vector<int> nums(size);
    for (int i = 0; i < size; i++) {
        cin >> nums[i];
    }

    int queryNums;
    cin >> queryNums;

    for (int i = 0; i < queryNums; i++) {
        int temp;
        cin >> temp;

        auto ans = lower_bound(nums.begin(), nums.end(), temp);
        int idx = ans - nums.begin() + 1;

        if (ans != nums.end() && *ans == temp) {
            cout << "Yes " << idx << '\n';
        } else {
            cout << "No " << idx << '\n';
        }
    }

    return 0;
}
```
11. [Box It!](https://www.hackerrank.com/challenges/box-it/problem?isFullScreen=true)
```cpp
#include<bits/stdc++.h>

using namespace std;

//Implement the class Box  
//l,b,h are integers representing the dimensions of the box

// The class should have the following functions : 

// Constructors: 
// Box();
// Box(int,int,int);
// Box(Box);


// int getLength(); // Return box's length
// int getBreadth (); // Return box's breadth
// int getHeight ();  //Return box's height
// long long CalculateVolume(); // Return the volume of the box

//Overload operator < as specified
//bool operator<(Box& b)

//Overload operator << as specified
//ostream& operator<<(ostream& out, Box& B)

class Box{
    private:
    int l;
    int b;
    int h;
    
    public:
    
    Box(){
        l = 0;
        b = 0;
        h = 0;
    }
    
    Box (int _l, int _b, int _h){
        l = _l;
        b = _b;
        h = _h;
    }
    
    Box (const Box& other){
        l = other.l;
        b = other.b;
        h = other.h;
    }
    
    void NewBox(int a, int c, int e){
        l = a;
        b = c;
        h = e;
    }
    
    long long CalculateVolume() const{
        return 1LL*l*b*h;
    }
    
    int getBreadth() const{
        return b;
    }
    int getHeight() const{
        return h;
    }
    int getLength() const{
        return l;
    }
    
    bool operator<(const Box& other) const{
        if (l < other.l ){
            return true;
        }else if (b < other.b && l == other.l){
            return true;
        }else if (h < other.h && b == other.b && l == other.l){
            return true;
        }else{
            return false;
        }
    }
};


ostream& operator<<(ostream& out, const Box& B){
    out << B.getLength() << " " << B.getBreadth() << " " << B.getHeight();
    return out;
}


void check2()
{
	int n;
	cin>>n;
	Box temp;
	for(int i=0;i<n;i++)
	{
		int type;
		cin>>type;
		if(type ==1)
		{
			cout<<temp<<endl;
		}
		if(type == 2)
		{
			int l,b,h;
			cin>>l>>b>>h;
			Box NewBox(l,b,h);
			temp=NewBox;
			cout<<temp<<endl;
		}
		if(type==3)
		{
			int l,b,h;
			cin>>l>>b>>h;
			Box NewBox(l,b,h);
			if(NewBox<temp)
			{
				cout<<"Lesser\n";
			}
			else
			{
				cout<<"Greater\n";
			}
		}
		if(type==4)
		{
			cout<<temp.CalculateVolume()<<endl;
		}
		if(type==5)
		{
			Box NewBox(temp);
			cout<<NewBox<<endl;
		}

	}
}

int main()
{
	check2();
}
```
12. 
