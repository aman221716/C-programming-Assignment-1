//Question 1 : What do you mean by structures?
//Answer 1 :
#include <stdio.h>
#include <string.h>
// Structure: a user-defined data type that groups different data types together
struct Student {
    char name[20];
    int marks;
};
int main() {
    struct Student s1 = {"Student1", 90};
    printf("Name: %s\n", s1.name);
    printf("Marks: %d\n", s1.marks);
    return 0;
}
//Output :-
Name: Student1
Marks: 90
//Question 2: what do you mean by array and pointers array? 
//Answer 2: 
#include <stdio.h>

int main() {
    int marks[3] = {75, 85, 95};   // Normal array
    int *ptr[3] = {&marks[0], &marks[1], &marks[2]}; // Pointer array

    printf("Array: ");
    for(int i=0; i<3; i++) printf("%d ", marks[i]);
    printf("\n");

    printf("Pointer Array: ");
    for(int i=0; i<3; i++) printf("%d ", *ptr[i]);
    printf("\n");

    return 0;
}
// Output :-
Array: 75 85 95 
Pointer Array: 75 85 95

//Question 3: Compare two structures variables by using the comparison operator (not equal and equal). 
//Answer 3: 
#include <stdio.h>
#include <string.h>
struct Student {
    char name[20];
    int marks;
};
int main() {
    struct Student s1 = {"Student1", 90};
    struct Student s2 = {"Student2)", 85};
    if(strcmp(s1.name, s2.name) == 0 && s1.marks == s2.marks)
        printf("Structures are equal\n");
    else
        printf("Structures are NOT equal\n");
    return 0;
} 
// Output :-
Structures are NOT equal

//Question 4: Perform an arithmetic operations on structures. 
//Answer 4:
#include <stdio.h>
struct Student {
    char name[20];
    int marks;
};
int main() {
    struct Student s1 = {"Student1", 90};
    struct Student s2 = {"Student2", 85};
    int totalMarks = s1.marks + s2.marks;
    int diffMarks = s1.marks - s2.marks;
    printf("Total marks: %d\n", totalMarks);
    printf("Difference of marks: %d\n", diffMarks);
    return 0;
}
//Output :-
Total marks: 175
Difference of marks: 5
