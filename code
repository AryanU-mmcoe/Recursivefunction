#include <stdio.h>
#include <string.h>

char input_word[20];
int count = 0;

void swap(char *x, char *y) {
    char temp;
    temp = *x;
    *x = *y;
    *y = temp;
}

void permute(char *str, int l, int r) {
    int i;
    if (l == r) {
        printf("%s\n", str);
        count++;
    } else {
        for (i = l; i <= r; i++) {
            swap((str + l), (str + i));
            permute(str, l + 1, r);
            swap((str + l), (str + i));
        }
    }
}

int main() {
    printf("Enter your word: ");
    scanf("%s", input_word);

    int length = strlen(input_word);


    printf("All permutations of \"%s\":\n", input_word);
    permute(input_word, 0, length - 1);
    
    printf("Total number of permutations: %d\n", count);

    return 0;
}
