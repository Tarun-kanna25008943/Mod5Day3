# EX-03 Program to Find the Sum of Major and Minor Diagonal Elements of a 3×3 Matrix

## AIM:
To write a C program to read a 3×3 matrix and calculate the sum of its major (main) and minor (off) diagonal elements.

## ALGORITHM:
1. Start
2. Declare a 3×3 integer array arr[3][3].
3. Read all elements of the matrix using nested loops.
4. Display the matrix.
5. Initialize majsum = 0, minsum = 0.
6. For each i from 0 to 2:
   * Add arr[i][i] to majsum (major diagonal).
   * Add arr[i][2 - i] to minsum (minor diagonal).
7. Print both diagonal elements and their sums.
8. Stop

## PROGRAM:
```
#include <stdio.h>

int main()
{
    int num = 3;
    int arr[num][num];
    
    printf("Enter the matrix: \n");
    
    for(int i = 0; i < num; i++)
    {
        for(int j = 0; j < num; j++)
        {
            scanf("%d",&arr[i][j]);
        }
    }
    
    printf("\nThe entered matrix is: \n");
    
    for(int i = 0; i < num; i++)
    {
        for(int j = 0; j < num; j++)
        {
            printf("%d ",arr[i][j]);
        }
        printf("\n");
    }
    
    printf("\nMajor Diagonal Elements : ");
    int majsum = 0;
    
    for(int i = 0; i < num; i++)
    {
        printf("%d ",arr[i][i]);
        majsum = majsum + arr[i][i];
    }
    
    printf("\n\nMinor Diagonal Elements : ");
    
    int count = num-1;
    int minsum = 0;
    for(int i = 0; i < num; i++)
    {
        for(int j = 0; j < num; j++)
        {
            if(j == count)
            {
                printf("%d ",arr[i][j]);
                minsum = minsum + arr[i][j];
            }
        }
        count--;
    }
    
    printf("\n\nSum of Major Diagonal Elements : %d",majsum);
    printf("\n\nSum of Minor Diagonal Elements : %d",minsum);
    
    
    
    return 0;
}
```

## OUTPUT:
<img width="666" height="465" alt="image" src="https://github.com/user-attachments/assets/22c2172a-5950-4f00-977a-ffadbdb950a4" />

## RESULT:
The program successfully reads a 3×3 matrix and calculates the sum of its main and minor diagonal elements.
