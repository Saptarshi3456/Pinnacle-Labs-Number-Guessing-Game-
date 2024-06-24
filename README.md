# Pinnacle-Labs-Number-Guessing-Game-
Build a number guessing game in C where the program generates a random number and the user tries to save it.
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main() {
    srand(time(NULL)); // Seed random number generator
    int numberToGuess = rand() % 100 + 1; // Generate random number between 1 and 100
    int guess;
    int attempts = 0;

    printf("Guess a number between 1 and 100:\n");

    while (1) {
        scanf("%d", &guess);
        attempts++;

        if (guess < numberToGuess) {
            printf("Too low! Try again:\n");
        } else if (guess > numberToGuess) {
            printf("Too high! Try again:\n");
        } else {
            printf("Congratulations! You found the number in %d attempts.\n", attempts);
            break;
        }
    }

    return 0;
}
