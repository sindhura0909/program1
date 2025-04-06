#include <stdio.h>

void reverseArray(int arr[], int size) {
    int temp;
    for(int i = 0; i < size / 2; i++) {
        // Swap elements at i and (size - i - 1)
        temp = arr[i];
        arr[i] = arr[size - i - 1];
        arr[size - i - 1] = temp;
    }
}

void printArray(int arr[], int size) {
    for(int i = 0; i < size; i++) {
        printf("%d ", arr[i]);
    }
    printf("\n");
}

int main() {
    int arr[] = {1, 2, 3, 4, 5};
    int size = sizeof(arr) / sizeof(arr[0]);

    printf("Original array:\n");
    printArray(arr, size);

    reverseArray(arr, size);

    printf("Reversed array:\n");
    printArray(arr, size);

    return 0;
}# program1
