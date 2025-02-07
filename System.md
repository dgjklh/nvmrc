#include <iostream>
#include <vector>
using namespace std;

struct Student {
    string name;
    double grade;
};

int main() {
    vector<Student> students;
    string name;
    double grade;
    
    while (true) {
        cout << "Enter student name (or 'exit' to stop): ";
        cin >> name;
        if (name == "exit") break;
        
        cout << "Enter grade: ";
        cin >> grade;
        students.push_back({name, grade});
    }

    cout << "\nStudent Grades:\n";
    for (auto &s : students) {
        cout << s.name << ": " << s.grade << endl;
    }

    return 0;
}
