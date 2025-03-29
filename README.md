# Matrix-Data-Structure
## Given two N x M matrices. Find a N x M matrix as the sum of given matrices each value at the sum of values of corresponding elements of the given two matrices. In this article, we will learn about the addition of two matrices.

<img src="https://media.geeksforgeeks.org/wp-content/uploads/20230627124621/C-Program-For-Addition-of-Two-Matrices.png">

# Approach
Below is the idea to solve the problem.

Iterate over every cell of the matrix (i, j).
Add the corresponding values of the two matrices.
Store in a single matrix i.e. the resultant matrix.

# Algorithm : 
```
Initialize a resultant matrix res[N][M].
Run a for loop for counter i as each row and in each iteration:
Run a for loop for counter j as each column and in each iteration:
Add values of the two matrices for index i, j, and store in res[i][j].
Return res.
```

# Code :

```
// C++ program for addition
// of two matrices
#include <bits/stdc++.h>
using namespace std;
#define N 4

// This function adds A[][] and B[][],
// and stores the result in C[][]
void add(int A[][N], int B[][N], int C[][N])
{
    int i, j;
    for (i = 0; i < N; i++)
        for (j = 0; j < N; j++)
            C[i][j] = A[i][j] + B[i][j];
}

// Driver code
int main()
{
    int A[N][N] = { { 1, 1, 1, 1 },
                    { 2, 2, 2, 2 },
                    { 3, 3, 3, 3 },
                    { 4, 4, 4, 4 } };

    int B[N][N] = { { 1, 1, 1, 1 },
                    { 2, 2, 2, 2 },
                    { 3, 3, 3, 3 },
                    { 4, 4, 4, 4 } };

    // To store the result
    int C[N][N];
    int i, j;
    add(A, B, C);

    cout << "Result matrix is " << endl;
    for (i = 0; i < N; i++) {
        for (j = 0; j < N; j++)
            cout << C[i][j] << " ";
        cout << endl;
    }

    return 0;
}

```

# Output 
```
Result matrix is 
2 2 2 2 
4 4 4 4 
6 6 6 6 
8 8 8 8
```
# Complexity
Time Complexity : O(n2)
<br>
Auxiliary Space : O(n2)
