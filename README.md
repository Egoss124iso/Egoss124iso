#include <iostream>
#include <map>
#include <string>
#include <stdlib.h>

using namespace std;

void login();
void Registr();
void forgot();

// Temporary in-memory storage for users (username -> password)
map<string, string> users;

int main() {
    int choice;
    while (true) {
        cout << "********************" << endl;
        cout << "*****WELCOME********" << endl;
        cout << "MENU:" << endl;
        cout << "1. Login" << endl;
        cout << "2. Register" << endl;
        cout << "3. Forgot Username or Password" << endl;
        cout << "4. Exit" << endl;
        cout << "Enter your Choice: ";
        cin >> choice;
        cout << endl;

        switch (choice) {
            case 1:
                login();
                break;
            case 2:
                Registr();
                break;
            case 3:
                forgot();
                break;
            case 4:
                cout << "Exiting... Goodbye!" << endl;
                return 0;
            default:
                cout << "Invalid choice, please try again." << endl;
        }
    }
}

void login() {
    string user, pass;
    system("cls");
    cout << "Please Enter the following details: " << endl;
    cout << "Username: ";
    cin >> user;
    cout << "Password: ";
    cin >> pass;

    // Check if user exists in the temporary map
    if (users.find(user) != users.end() && users[user] == pass) {
        system("cls");
        cout << "Hello " << user << "\n<LOGIN SUCCESSFUL>\n";
    } else {
        cout << "\nLOGIN ERROR! Please check your username and password." << endl;
    }
}

void Registr() {
    string reguser, regpass;
    system("cls");
    cout << "Enter the Username: ";
    cin >> reguser;
    cout << "Enter the Password: ";
    cin >> regpass;

    // Add the user to the temporary in-memory storage
    if (users.find(reguser) == users.end()) {
        users[reguser] = regpass;
        cout << "\nRegistration Successful!" << endl;
    } else {
        cout << "Error: Username already exists. Please try a different one." << endl;
    }
}

void forgot() {
    string searchuser;
    system("cls");
    cout << "Forgotten? We're here to help." << endl;
    cout << "Enter your remembered username: ";
    cin >> searchuser;

    // Check if the username exists in the temporary map
    if (users.find(searchuser) != users.end()) {
        cout << "\nAccount Found!" << endl;
        cout << "Your Password is: " << users[searchuser] << endl;
    } else {
        cout << "\nSorry, your user ID is not found in our temporary storage." << endl;
    }
}#include <iostream>
#include <map>
#include <string>
#include <stdlib.h>

using namespace std;

void login();
void Registr();
void forgot();

// Temporary in-memory storage for users (username -> password)
map<string, string> users;

int main() {
    int choice;
    while (true) {
        cout << "********************" << endl;
        cout << "*****WELCOME********" << endl;
        cout << "MENU:" << endl;
        cout << "1. Login" << endl;
        cout << "2. Register" << endl;
        cout << "3. Forgot Username or Password" << endl;
        cout << "4. Exit" << endl;
        cout << "Enter your Choice: ";
        cin >> choice;
        cout << endl;

        switch (choice) {
            case 1:
                login();
                break;
            case 2:
                Registr();
                break;
            case 3:
                forgot();
                break;
            case 4:
                cout << "Exiting... Goodbye!" << endl;
                return 0;
            default:
                cout << "Invalid choice, please try again." << endl;
        }
    }
}

void login() {
    string user, pass;
    system("cls");
    cout << "Please Enter the following details: " << endl;
    cout << "Username: ";
    cin >> user;
    cout << "Password: ";
    cin >> pass;

    // Check if user exists in the temporary map
    if (users.find(user) != users.end() && users[user] == pass) {
        system("cls");
        cout << "Hello " << user << "\n<LOGIN SUCCESSFUL>\n";
    } else {
        cout << "\nLOGIN ERROR! Please check your username and password." << endl;
    }
}

void Registr() {
    string reguser, regpass;
    system("cls");
    cout << "Enter the Username: ";
    cin >> reguser;
    cout << "Enter the Password: ";
    cin >> regpass;

    // Add the user to the temporary in-memory storage
    if (users.find(reguser) == users.end()) {
        users[reguser] = regpass;
        cout << "\nRegistration Successful!" << endl;
    } else {
        cout << "Error: Username already exists. Please try a different one." << endl;
    }
}

void forgot() {
    string searchuser;
    system("cls");
    cout << "Forgotten? We're here to help." << endl;
    cout << "Enter your remembered username: ";
    cin >> searchuser;

    // Check if the username exists in the temporary map
    if (users.find(searchuser) != users.end()) {
        cout << "\nAccount Found!" << endl;
        cout << "Your Password is: " << users[searchuser] << endl;
    } else {
        cout << "\nSorry, your user ID is not found in our temporary storage." << endl;
    }
}
