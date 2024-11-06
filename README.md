# Cat-2            
1)#include <stdio.h>
#include <string.h>

// Define the Employee structure
struct Employee {
    char name[25];
    int ID;
    char department[20];
    float salary;
    char email[50];
};

int main() {
    // Declare and initialize an Employee variable
    struct Employee emp = {
        "John Doe",             // name
        12345,                  // ID
        "Human Resource",       // department
        55000.50,                // salary
        "johndoe@company.com"   // email
    };

    // Print the values of the Employee
    printf("Employee Details:\n");
    printf("Name: %s\n", name);
    printf("ID: %d\n", ID);
    printf("Department: %s\n", department);
    printf("Salary: %.2f\n", salary);
    printf("Email: %s\n", email);

    return 0;
}

qn 2)1)An array is a data structure in programming that stores a fixed-size sequence of elements, all of which are of the same data type.

2)#include <stdio.h>

int main() {
    // Declare and initialize a 2D array with 2 rows and 4 columns
    int SCORES[2][4] = {
        {65, 95, 35, 70},  // First row
        {84, 72, 59, 67}   // Second row
    };

    // Print the elements of the array
    printf("SCORES[0][0]: %d\n", SCORES[0][0]);
    printf("SCORES[0][1]: %d\n", SCORES[0][1]);
    printf("SCORES[0][2]: %d\n", SCORES[0][2]);
    printf("SCORES[0][3]: %d\n", SCORES[0][3]);
    
    printf("SCORES[1][0]: %d\n", SCORES[1][0]);
    printf("SCORES[1][1]: %d\n", SCORES[1][1]);
    printf("SCORES[1][2]: %d\n", SCORES[1][2]);
    printf("SCORES[1][3]: %d\n", SCORES[1][3]);

    return 0;
}

3)#include <stdio.h>

int main() {
    // Declare and initialize a 2D array with 2 rows and 4 columns
    int SCORES[2][4] = {
        {65, 95, 35, 70},  // First row
        {84, 72, 59, 67}   // Second row
    };

    // Use nested for loop to print the elements of the array
    for (int i = 0; i < 2; i++) {  
        for (int j = 0; j < 4; j++) {  
            printf("SCORES[%d][%d]: %d\n", i, j, SCORES[i][j]);
        }
    }

    return 0;
}

qn 3)#include <stdio.h>

int main() {
    float hoursWorked, hourlyWage, grossPay, taxes, netPay;
    float overtimeRate = 1.5;
    float taxRate1 = 0.15, taxRate2 = 0.20;
    float taxThreshold = 600.0;

    // Request user input
    printf("Enter hours worked in a week: ");
    scanf("%f", &hoursWorked);
    printf("Enter hourly wage: ");
    scanf("%f", &hourlyWage);

    // Calculate gross pay
    if (hoursWorked <= 40) {
        grossPay = hoursWorked * hourlyWage;  // No overtime
    } else {
        // Calculate overtime
        float regularHours = 40;
        float overtimeHours = hoursWorked - regularHours;
        grossPay = (regularHours * hourlyWage) + (overtimeHours * hourlyWage * overtimeRate);  // Overtime pay
    }

    // Calculate taxes
    if (grossPay <= taxThreshold) {
        taxes = grossPay * taxRate1;  // 15% tax on the first $600
    } else {
        taxes = (taxThreshold * taxRate1) + ((grossPay - taxThreshold) * taxRate2);  // 15% on first $600, 20% on the rest
    }

    // Calculate net pay
    netPay = grossPay - taxes;

    // Display results
    printf("\nGross Pay: $%.2f\n", grossPay);
    printf("Taxes: $%.2f\n", taxes);
    printf("Net Pay: $%.2f\n", netPay);

    return 0;
}



