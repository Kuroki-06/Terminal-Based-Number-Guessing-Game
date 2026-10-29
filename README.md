Terminal-Based-Number-Guessing-Game
#include <stdio.h>
#include <unistd.h>


int main()
{
    int guessing_n = 0, n = 20, i, ln = 0;

    ln = guessing_n;

    printf("The game will start in three seconds.\n");

    for(i = 3; i >= 1; i--)
    {
        printf("%d\n", i);
        sleep(1);
    }

    printf("Game Start\n");
    printf("Guess the correct number from 1-100\n");

    do
    {
        scanf("%d", &guessing_n);
        if(guessing_n > n)
        {
            printf("Try lower.\n");
        }
        else if(guessing_n < n)
        {
            printf("Try higher.\n");
        }
        else
        {break;}

        if(guessing_n > ln)
        {
            ln = guessing_n;
        }

    }while(guessing_n != n);

    printf("Good job. You guessed the correct number!\n");
    printf("You win!\n");
    printf("The greatest number entered was %d", ln);

    return 0;
}
