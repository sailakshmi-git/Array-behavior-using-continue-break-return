# Array-behavior-using-continue-break-return
Write a C program that iterates through an array and, within a loop, uses continue  to skip negative elements, break when a zero is encountered, and return to exit the program if an element greater than 100 is found, then print the resulting behavior for the array {10, -5, 20, 0, 150, 30}.

Program:

```
#include <stdio.h>

int main() {
    int arr[] = {10, -5, 20, 0, 150, 30};
    int n = 6;

    for(int i = 0; i < n; i++) {

        if(arr[i] < 0) {
            printf("Skipping negative: %d\n", arr[i]);
            continue;
        }

        if(arr[i] == 0) {
            printf("Zero found. Breaking loop.\n");
            break;
        }

        if(arr[i] > 100) {
            printf("Value > 100 found (%d). Exiting program.\n", arr[i]);
            return 0;
        }

        printf("Processing: %d\n", arr[i]);
    }

    printf("Program ended normally.\n");
    return 0;
}
```

Output:

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/70709e4f-ae6b-4925-929a-3c4bb4ea0f59" />
