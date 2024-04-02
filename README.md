# c-program
#include <stdio.h>
#include <string.h>

#define MAX_USERNAME_LENGTH 50
#define MAX_PASSWORD_LENGTH 50

int main() {
    char username[MAX_USERNAME_LENGTH];
    char password[MAX_PASSWORD_LENGTH];

    printf("Welcome to the Login Page!\n");

    // Read username
    printf("Enter your username: ");
    fgets(username, MAX_USERNAME_LENGTH, stdin);
    username[strcspn(username, "\n")] = '\0'; // Remove the newline character

    // Read password
    printf("Enter your password: ");
    fgets(password, MAX_PASSWORD_LENGTH, stdin);
    password[strcspn(password, "\n")] = '\0'; // Remove the newline character

    // Simple validation (replace this with your actual authentication logic)
    if (strcmp(username, "admin") == 0 && strcmp(password, "admin") == 0) {
        printf("Login successful!\n");
        // Proceed to main application or perform necessary actions
    } else {
        printf("Invalid username or password. Please try again.\n");
    }

    return 0;
}
