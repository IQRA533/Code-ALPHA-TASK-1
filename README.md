# Code-ALPHA-TASK-1#include <iostream>
#include <iomanip>
using namespace std;

int main() 
{
    int numCourses;
    string grade;
    int creditHours;
    float gradePoint, totalGradePoints = 0, totalCredits = 0, cgpa;

    cout << "========== CGPA Calculator ==========" << endl;

    
    cout << "Enter number of courses: ";
    cin >> numCourses;

    for (int i = 1; i <= numCourses; i++) 
    {
        cout << "\nCourse " << i << endl;

        
        cout << "Enter grade (A, B, C, D, F): ";
        cin >> grade;

        
        cout << "Enter credit hours: ";
        cin >> creditHours;

        
        if (grade == "A" || grade == "a")
            gradePoint = 4.0;
        else if (grade == "B" || grade == "b")
            gradePoint = 3.0;
        else if (grade == "C" || grade == "c")
            gradePoint = 2.0;
        else if (grade == "D" || grade == "d")
            gradePoint = 1.0;
        else
            gradePoint = 0.0;

        
        totalGradePoints += gradePoint * creditHours;
        totalCredits += creditHours;

    
        cout << "Grade: " << grade << endl;
        cout << "Credit Hours: " << creditHours << endl;
        cout << "Grade Points: " << gradePoint << endl;
    }

    
    cgpa = totalGradePoints / totalCredits;

    
    cout << "\n========== Result ==========" << endl;
    cout << "Total Credit Hours = " << totalCredits << endl;
    cout << "Total Grade Points = " << totalGradePoints << endl;
    cout << fixed << setprecision(2);
    cout << "Final CGPA = " << cgpa << endl;

    return 0;
}
