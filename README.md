# Working-function-of-ATM-machine-c++

#include <stdio.h>
#include <string.h>
#include <ctype.h>

int main() {
    char password[100];
    int i;
    int hasUpper = 0, hasLower = 0, hasDigit = 0, hasSpecial = 0;

    printf("Enter your password: ");
    scanf("%s", password);

    int length = strlen(password);

    // Check each character
    for(i = 0; i < length; i++) {
        if(isupper(password[i]))
            hasUpper = 1;
        else if(islower(password[i]))
            hasLower = 1;
        else if(isdigit(password[i]))
            hasDigit = 1;
        else
            hasSpecial = 1;
    }

    // Strength checking
    if(length >= 8 && hasUpper && hasLower && hasDigit && hasSpecial) {
        printf("Password Strength: STRONG\n");
    }
    else if(length >= 6 && ((hasUpper && hasLower) || (hasDigit && hasSpecial))) {
        printf("Password Strength: MEDIUM\n");
    }
    else {
        printf("Password Strength: WEAK\n");
    }

    return 0;
}#include <stdio.h>
#include <string.h>
#include <ctype.h>

int main() {
    char password[100];
    int i;
    int hasUpper = 0, hasLower = 0, hasDigit = 0, hasSpecial = 0;

    printf("Enter your password: ");
    scanf("%s", password);

    int length = strlen(password);

    // Check each character
    for(i = 0; i < length; i++) {
        if(isupper(password[i]))
            hasUpper = 1;
        else if(islower(password[i]))
            hasLower = 1;
        else if(isdigit(password[i]))
            hasDigit = 1;
        else
            hasSpecial = 1;
    }

    // Strength checking
    if(length >= 8 && hasUpper && hasLower && hasDigit && hasSpecial) {
        printf("Password Strength: STRONG\n");
    }
    else if(length >= 6 && ((hasUpper && hasLower) || (hasDigit && hasSpecial))) {
        printf("Password Strength: MEDIUM\n");
    }
    else {
        printf("Password Strength: WEAK\n");
    }

    return 0;
}
