#include <stdio.h>

int main(void)
{
    int unit_cons;
    int charge;
    int bill;

    printf("Enter the number of units consumed: ");

    if (scanf("%d", &unit_cons) != 1) {
        printf("Error: please enter a valid whole number.\n");
        return 1;
    }

    if (unit_cons < 0) {
        printf("Error: units consumed cannot be negative.\n");
        return 1;
    }

    if (unit_cons <= 100) {
        charge = 50;
    }
    else if (unit_cons <= 200) {
        charge = 75;
    }
    else {
        charge = 100;
    }

    bill = unit_cons * charge;

    printf("Units consumed: %d\n", unit_cons);
    printf("Charge per unit: %d\n", charge);
    printf("Your electricity bill is: %d\n", bill);

    return 0;
}

