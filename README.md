Program to Find all symmetric elements in an array in C
In this article , we will learn how to create a program to find all the symmetric elements in an array in C.The symmetric elements is said to be symmetric when in pairs say (a,b) and (c,d) in which ‘b’ is equal to ‘c’ and ‘a’ is equal to ‘d’.

Symmetic elements in an array
Explanation :
We are given with an array pairs, inside that array some symmetric pairs exist. The problem statement says that we have to find all symmetric pairs that exist in array. we can simply use two loops and traverse the 2d array.
Example,
Input : arr[5][2]={{1,2}, {3,4}, {5,6}, {2,1}, {4,3}}
Output : (1,2) (3,4)
Algorithm :
Declare a 2D array for pairs.
Run a outer loop from index  0 to 5
Run an inner loop from index i+1 to 5
Check if(arr[i][0]==arr[j][1] && arr[i][1]==arr[j][0])), then print the arr[i][0] and arr[i][1].
Time and Space Complexity :
Time Complexity : O(n2)
Space Complexity : O(1)
Related Pages
Finding Maximum scalar product of two vectors in an array

Counting the number of even and odd elements in an array

Find maximum product sub-array in a given array

Finding Arrays are disjoint or not

Determine Array is a subset of another array or not

Code in C
Run
#include<stdio.h>

int main()
{
   int arr[5][2];
   arr[0][0] = 1; arr[0][1] = 2;
   arr[1][0] = 3; arr[1][1] = 4;
   arr[2][0] = 5; arr[2][1] = 1;
   arr[3][0] = 4; arr[3][1] = 3;
   arr[4][0] = 1; arr[4][1] = 5;

   for(int i=0; i<5; i++){
      for(int j=i+1; j<5; j++){
         if(arr[i][0]==arr[j][1] && arr[i][1]==arr[j][0])
           printf("(%d, %d) ", arr[i][0], arr[i][1]);
      }
   }

   return 0;
}
Output
(3, 4) (5, 4)
