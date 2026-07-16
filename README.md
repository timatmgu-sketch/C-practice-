# C-practice-
# Simple Array Max Finder

How to use it :
1.Compile code: "gcc main.c -o findmax"
2.Start programm: "find_max" 

Code of a mini programm: 

#include <stdio.h>

/**
 * find_max - Finds a maximal number in array.
 * @ptr: Pointer on the array start.
 * @size: Quantati of elements in array.
 * 
 * Returns maximum number.
 */

int find_max(int *ptr,int size) {
    int max = ptr[0];

    for(int i = 0;i < size;i++) {
        if(ptr[i] > max) {
          max = ptr[i];
        }
    }
    return max;
}

 int main() {
    int arr [] = {1,6,17,30};
    int size = sizeof(arr) / sizeof(arr[0]); /** Automaticly calculates size */


    int result = find_max(arr,4);

    printf("Array:...\n");
    for(int i = 0;i < size;i++) {
        printf("%d\n",arr[i]);
    }
    
    printf("The maximum number in this array is %d\n",result);

    

    return 0;
}
