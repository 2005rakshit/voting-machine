#include <stdio.h>

int main() {
    int vote1 = 0, vote2 = 0, vote3 = 0;
    int choice;

    while (1) {
        printf("\n==== SIMPLE VOTING SYSTEM ====\n");
        printf("1. Vote for Candidate 1\n");
        printf("2. Vote for Candidate 2\n");
        printf("3. Vote for Candidate 3\n");
        printf("4. Show Vote Count\n");
        printf("5. Declare Winner\n");
        printf("6. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);

        if (choice == 1) {
            vote1++;
            printf("You voted for Candidate 1!\n");
        }
        else if (choice == 2) {
            vote2++;
            printf("You voted for Candidate 2!\n");
        }
        else if (choice == 3) {
            vote3++;
            printf("You voted for Candidate 3!\n");
        }
        else if (choice == 4) {
            printf("\n--- Vote Count ---\n");
            printf("Candidate 1: %d votes\n", vote1);
            printf("Candidate 2: %d votes\n", vote2);
            printf("Candidate 3: %d votes\n", vote3);
        }
        else if (choice == 5) {
            printf("\n=== Winner ===\n");
            if (vote1 > vote2 && vote1 > vote3)
                printf("Candidate 1 is the winner!\n");
            else if (vote2 > vote1 && vote2 > vote3)
                printf("Candidate 2 is the winner!\n");
            else if (vote3 > vote1 && vote3 > vote2)
                printf("Candidate 3 is the winner!\n");
            else
                printf("It's a tie!\n");
        }
        else if (choice == 6) {
            printf("Exiting program...\n");
            break;
        }
        else {
            printf("Invalid choice! Try again.\n");
        }
    }

    return 0;
}
