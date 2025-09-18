#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main()
{
    int random, guess;
    int no_of_guess = 0;

    srand(time(NULL));  // Seed the random number generator

    printf("Welcome to the world of guessing numbers!\n");

    random = rand() % 100 + 1;  // Generate number between 1 and 100

    // Debug only – comment out in final version
    // printf("Number generated is: %d\n", random);

    do
    {
        printf("\nPlease enter your guess between 1 and 100: ");
        scanf("%d", &guess);
        no_of_guess++;

        if (guess < random)
        {
            printf("Guess a larger number.\n");
        }
        else if (guess > random)
        {
            printf("Guess a smaller number.\n");
        }
        else
        {
            printf("Congratulations! You have successfully guessed the number in %d attempts.\n", no_of_guess);
        }

    } while (guess != random);

    printf("\nBye bye, thank you for playing.");
    printf("\nDeveloped by: Vikash Kushwah\n");

    return 0;
}
