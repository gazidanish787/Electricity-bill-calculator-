
#include <stdio.h>

int main() {
    int units;
    float amount;

    printf("Enter electricity units consumed: ");
    scanf("%d", &units);

    if(units <= 100) {
        amount = units * 5.0;          // 5 Rs per unit
    }
    else if(units <= 200) {
        amount = (100 * 5.0) + (units - 100) * 7.0;
    }
    else if(units <= 300) {
        amount = (100 * 5.0) + (100 * 7.0) + (units - 200) * 10.0;
    }
    else {
        amount = (100 * 5.0) + (100 * 7.0) + (100 * 10.0) + (units - 300) * 15.0;
    }

    printf("Total Electricity Bill = Rs %.2f\n", amount);

    return 0;
}
