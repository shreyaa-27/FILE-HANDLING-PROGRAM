// Standard input-output library for file handling
#include <stdio.h>
// Standard library for general utilities
#include <stdlib.h>

int main() {
    // File pointer initialized to NULL for safety
    FILE *file = NULL;
    // Variable to store filename
    char filename[100];
    // Variable to store user choice
    int choice;
    // Buffer to store user input
    char data[100];
    
    // Ask user for filename
    printf("Enter filename: ");
    scanf("%s", filename);
    getchar(); // Consume newline character
    
    do {
        // Display menu options
        printf("\n1. Write to File\n2. Read from File\n3. Append to File\n4. Exit\nEnter choice: ");
        scanf("%d", &choice);
        getchar(); // To consume the newline left by scanf
        
        switch (choice) {
            case 1:
                // Open file in write mode (overwrites existing content)
                file = fopen(filename, "w");
                printf("Enter text: ");
                fgets(data, sizeof(data), stdin);
                fputs(data, file);
                fclose(file);
                break;
            case 2:
                // Open file in read mode
                file = fopen(filename, "r");
                if (file == NULL) {
                    printf("File not found!\n");
                    break;
                }
                // Read and display file content line by line
                while (fgets(data, sizeof(data), file))
                    printf("%s", data);
                fclose(file);
                break;
            case 3:
                // Open file in append mode (preserves existing content)
                file = fopen(filename, "a");
                printf("Enter text to append: ");
                fgets(data, sizeof(data), stdin);
                fputs(data, file);
                fclose(file);
                break;
            case 4:
                // Exit message
                printf("Exiting...\n");
                break;
            default:
                // Handle invalid user input
                printf("Invalid choice!\n");
        }
    } while (choice != 4);
    
    return 0;
}
