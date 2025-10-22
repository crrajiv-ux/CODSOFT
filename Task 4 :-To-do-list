#include <iostream>
#include <vector>
#include <string>
using namespace std;

void showMenu() {
    cout << "\n=== TO-DO LIST MANAGER ===\n";
    cout << "1. Add Task\n";
    cout << "2. View Tasks\n";
    cout << "3. Delete Task\n";
    cout << "4. Exit\n";
    cout << "Choose an option: ";
}

int main() {
    vector<string> tasks;
    int choice;

    while (true) {
        showMenu();
        cin >> choice;
        cin.ignore(); // to handle newline after number input

        if (choice == 1) {
            string task;
            cout << "Enter your task: ";
            getline(cin, task);
            tasks.push_back(task);
            cout << "Task added successfully!\n";
        } 
        else if (choice == 2) {
            cout << "\nYour Tasks:\n";
            if (tasks.empty()) {
                cout << "No tasks found.\n";
            } else {
                for (size_t i = 0; i < tasks.size(); ++i) {
                    cout << i + 1 << ". " << tasks[i] << endl;
                }
            }
        } 
        else if (choice == 3) {
            int delIndex;
            cout << "Enter task number to delete: ";
            cin >> delIndex;
            if (delIndex > 0 && delIndex <= tasks.size()) {
                tasks.erase(tasks.begin() + delIndex - 1);
                cout << "Task deleted successfully!\n";
            } else {
                cout << "Invalid task number.\n";
            }
        } 
        else if (choice == 4) {
            cout << "Exiting program. Goodbye!\n";
            break;
        } 
        else {
            cout << "Invalid choice. Try again.\n";
        }
    }

    return 0;
}
