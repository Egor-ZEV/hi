#include <stdio.h>

// Функция для проверки, является ли число простым
int is_prime(int num) {
    if (num <= 1) {
        return 0; // Не является простым
    }
    for (int i = 2; i * i <= num; ++i) {
        if (num % i == 0) {
            return 0; // Не является простым
        }
    }
    return 1; // Является простым
}

int main() {
    int n;
    printf("Введите число: ");
    scanf("%d", &n);

    printf("Простые числа, включая %d:\n", n);
    for (int i = 2; i <= n; ++i) {
        if (is_prime(i)) {
            printf("%d ", i);
        }
    }
    printf("\n");

    return 0;
}