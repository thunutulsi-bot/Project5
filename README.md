#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main() {
    int user, computer;

    printf("Rock-Paper-Scissors Game\n");
    printf("1. Rock\n2. Paper\n3. Scissors\n");
    printf("Enter your choice (1-3): ");
    scanf("%d", &user);

    srand(time(0));
    computer = rand() % 3 + 1;

    printf("Computer chose: %d\n", computer);

    if (user == computer) {
        printf("It's a draw!\n");
    }
    else if ((user == 1 && computer == 3) ||
             (user == 2 && computer == 1) ||
             (user == 3 && computer == 2)) {
        printf("You win!\n");
    }
    else {
        printf("Computer wins!\n");
    }

    return 0;
}
